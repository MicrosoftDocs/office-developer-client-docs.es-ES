---
title: Compatibilidad con el subprocesamiento en los proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- multithreading [infopath 2007], infopath 2003-compatible form templates,threading [InfoPath 2007], support for projects using InfoPath 2003 object model,InfoPath 2003-compatible form templates, threading support
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: Los objetos COM a los que se obtiene acceso mediante los ensamblados de interoperabilidad Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll y Microsoft.Office.Interop.InfoPath.Xml.dll que instala Microsoft InfoPath no admiten la realización de llamadas en varios subprocesos. Esta regla se aplica también a las interfaces para objetos de Microsoft XML Core Services (MSXML) que se ajustan mediante el espacio de nombres Microsoft.Office.Interop.InfoPath.SemiTrust (la mayor parte de los cuales llevan el prefijo IXMLDOM) y a todas las interfaces que expone el espacio de nombres Microsoft.Office.Interop.InfoPath.Xml, que no son seguras para subprocesos.
ms.openlocfilehash: 1be2bd0181c47097440af54f1aa804a4f17b30bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299842"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a>Compatibilidad con el subprocesamiento en los proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003

Los objetos COM a los que se obtiene acceso mediante los ensamblados de interoperabilidad Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll y Microsoft.Office.Interop.InfoPath.Xml.dll que instala Microsoft InfoPath no admiten la realización de llamadas en varios subprocesos. Esto incluye las interfaces para los objetos de Microsoft XML Core Services (MSXML) que se ajustan mediante el espacio de nombres **Microsoft. Office. Interop. InfoPath. SemiTrust** (la mayoría de los cuales tienen nombres prefijados con IXMLDOM) y todas las interfaces expuestas por el espacio de nombres [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) , ninguno de los cuales es seguro para subprocesos. 
  
Todas las llamadas a estos objetos COM se deben realizar en un único subproceso. El código administrado de un proyecto de InfoPath puede crear otros subprocesos para realizar trabajo en segundo plano, pero el código que se ejecuta en subprocesos distintos del subproceso principal no puede llamar a los modelos de objetos de InfoPath.
  
Si su proyecto de código administrado de InfoPath utiliza un subprocesamiento múltiple, deberá tener cuidado a la hora de compartir objetos entre subprocesos. Los distintos subprocesos no deben compartir referencias al modelo de objetos de documento (DOM) XML ni a objetos de InfoPath. 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a>Realizar llamadas asincrónicas al modelo de objetos de InfoPath

En las situaciones en las que es necesario llamar a un proceso como, por ejemplo, un temporizador que se ejecute en un subproceso aparte, es posible solucionar el problema que supone el hecho que el modelo de objetos de InfoPath no admita este tipo de llamadas. 
  
En el siguiente ejemplo, se crea una instancia de **System.Timers.Timer** en el método _Startup del formulario y se enlaza una devolución de llamada asincrónica al temporizador. Además, se crea una instancia invisible del formulario de ventana (**System.Windows.Forms.Form**). Cuando la función de devolución de llamada transcurrido el intervalo temporizador se ejecuta una vez por segundo, llama a la función **PostMessage** de Win32 para enviar un mensaje a la ventana invisible. La ventana invisible dispone de una función **WndProc** que procesa el mensaje recibido desde la función de devolución de llamada del temporizador y actualiza el modelo de objetos de documento (DOM) XML del formulario. Para poder ejecutarse, el formulario se debe instalar como de plena confianza. Para obtener información sobre cómo depurar una plantilla de formulario de plena confianza, vea [vista previa y depurar plantillas de formulario que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md). Para obtener información sobre cómo implementar una plantilla de formulario de plena confianza, vea [implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md).
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
using System.Timers;
using System.Runtime.InteropServices;
// Office integration attribute. Identifies the startup class for the
// form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute("InfoPathStartupClass, Version=1.0, Class=AsyncUpdate.AsyncUpdate")]
namespace AsyncUpdate
{
    public class User32
    {
        [DllImport("User32.dll")]
        public static extern Int32 PostMessage(
            IntPtr hWnd, int Msg, int wParam, int lParam);
        public User32()
        {    
        }
        ~User32()
        {
        }
    }
    public class MyWindow : System.Windows.Forms.Form
    {
        private XDocument thisXDocument;
        private AsyncUpdate thisProcess ;
        // Private message for internal class.
        public const int WM_MYNOTIFY = 0x400;
        public MyWindow(XDocument doc, AsyncUpdate process)
        {
            thisXDocument = doc;
            thisProcess  = process;
            this.Text = "MyWindow";
            // Force HWND to get created in Win32
            IntPtr hwnd = this.Handle; 
        }
        [System.Security.Permissions.PermissionSet(System.Security.Permissions.SecurityAction.Demand, Name="FullTrust")]
        protected override void WndProc(
            ref System.Windows.Forms.Message m) 
        {
            switch (m.Msg)
            {
            case WM_MYNOTIFY:
                IXMLDOMNode xml = thisXDocument.DOM.selectSingleNode(
                    "/my:myFields/my:field1");
                xml.text = thisProcess.counter.ToString();
                break;                
            }
            base.WndProc(ref m);
        }
    }
    // The namespace prefixes defined in this attribute must remain 
    // synchronized with those in the form definition file (.xsf).
    [InfoPathNamespace("xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
    public class AsyncUpdate
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public int counter;
        private System.Timers.Timer myTimer;
        private MyWindow myWnd;
    
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // init the counter
            counter = 0;
            // Start a timer on another thread
            myTimer = new System.Timers.Timer(1000);
            myTimer.Elapsed += new ElapsedEventHandler(
                myTimer_Elapsed);
            myTimer.Start();
            // create hidden window to receive notifications 
            // back on the main thread
            myWnd = new MyWindow(thisXDocument, this);
        }
        public void _Shutdown()
        {
            myWnd.Dispose();
            myTimer.Stop();
            myTimer.Dispose();
        }
        private void myTimer_Elapsed(object sender, ElapsedEventArgs e)
        {
            // This method is called on a second thread
            counter ++;
            // Post message back to main thread
            User32.PostMessage(
                myWnd.Handle, MyWindow.WM_MYNOTIFY, 0, 0);
        }
    }
}

```



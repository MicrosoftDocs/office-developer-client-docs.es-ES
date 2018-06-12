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
ms.openlocfilehash: 314ef57e11295c0b2dbc9866c5faa392aab055ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815966"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a><span data-ttu-id="1e037-105">Compatibilidad con el subprocesamiento en los proyectos de InfoPath mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="1e037-105">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="1e037-106">Los objetos COM a los que se obtiene acceso mediante los ensamblados de interoperabilidad Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll y Microsoft.Office.Interop.InfoPath.Xml.dll que instala Microsoft InfoPath no admiten la realización de llamadas en varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1e037-106">The COM objects accessed through the Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll, and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies installed by Microsoft InfoPath do not support calls made on multiple threads.</span></span> <span data-ttu-id="1e037-107">Esto incluye las interfaces para los objetos de Microsoft XML Core Services (MSXML) que se ajustan mediante el espacio de nombres **Microsoft.Office.Interop.InfoPath.SemiTrust** (la mayoría de los cuales tienen nombres que van precedidos de IXMLDOM) y todas las interfaces expuestas por el espacio de nombres [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , ninguno de los cuales son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1e037-107">This includes the interfaces for Microsoft XML Core Services (MSXML) objects that are wrapped by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace (most of which have names that are prefixed with IXMLDOM) and all of the interfaces exposed by the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml)  namespace, none of which are thread-safe.</span></span> 
  
<span data-ttu-id="1e037-p103">Todas las llamadas a estos objetos COM se deben realizar en un único subproceso. El código administrado de un proyecto de InfoPath puede crear otros subprocesos para realizar trabajo en segundo plano, pero el código que se ejecuta en subprocesos distintos del subproceso principal no puede llamar a los modelos de objetos de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1e037-p103">All calls made to these COM objects must be issued on a single thread. Managed code in an InfoPath project can create other threads to perform background work, but code running on threads other than the main thread cannot call into the InfoPath object models.</span></span>
  
<span data-ttu-id="1e037-p104">Si su proyecto de código administrado de InfoPath utiliza un subprocesamiento múltiple, deberá tener cuidado a la hora de compartir objetos entre subprocesos. Los distintos subprocesos no deben compartir referencias al modelo de objetos de documento (DOM) XML ni a objetos de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1e037-p104">If your InfoPath managed code project uses multiple threads, you must be careful about sharing objects between threads. No references to the XML Document Object Model (DOM) or references to InfoPath objects should be shared between threads.</span></span> 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a><span data-ttu-id="1e037-112">Realizar llamadas asincrónicas al modelo de objetos de InfoPath</span><span class="sxs-lookup"><span data-stu-id="1e037-112">Making Asynchronous Calls to the InfoPath Object Model</span></span>

<span data-ttu-id="1e037-113">En las situaciones en las que es necesario llamar a un proceso como, por ejemplo, un temporizador que se ejecute en un subproceso aparte, es posible solucionar el problema que supone el hecho que el modelo de objetos de InfoPath no admita este tipo de llamadas.</span><span class="sxs-lookup"><span data-stu-id="1e037-113">For situations where it is necessary to call into a process such as a timer running on a separate thread, it is possible to work around the fact that the InfoPath object model does not support such calls.</span></span> 
  
<span data-ttu-id="1e037-114">En el siguiente ejemplo, se crea una instancia de **System.Timers.Timer** en el método _Startup del formulario y se enlaza una devolución de llamada asincrónica al temporizador.</span><span class="sxs-lookup"><span data-stu-id="1e037-114">The following example creates a **System.Timers.Timer** instance in the _Startup method of the form and hooks up an asynchronous callback to the timer.</span></span> <span data-ttu-id="1e037-115">Además, se crea una instancia del formulario de ventana (**System.Windows.Forms.Form**) invisible.</span><span class="sxs-lookup"><span data-stu-id="1e037-115">In addition, an invisible instance of the window form (**System.Windows.Forms.Form**) is created.</span></span> <span data-ttu-id="1e037-116">Cuando la función de devolución de llamada transcurrido el intervalo temporizador se ejecuta una vez por segundo, llama a la función **PostMessage** de Win32 para enviar un mensaje a la ventana invisible.</span><span class="sxs-lookup"><span data-stu-id="1e037-116">When the timer elapsed callback function executes once per second, it calls into the Win32 **PostMessage** function to post a message to the invisible window.</span></span> <span data-ttu-id="1e037-117">La ventana invisible dispone de una función **WndProc** que procesa el mensaje recibido desde la función de devolución de llamada del temporizador y actualiza el modelo de objetos de documento (DOM) XML del formulario.</span><span class="sxs-lookup"><span data-stu-id="1e037-117">The invisible window has a **WndProc** function that processes the message it receives from the timer callback function, and updates the XML document object model (DOM) of the form.</span></span> <span data-ttu-id="1e037-118">Para poder ejecutarse, el formulario se debe instalar como de plena confianza.</span><span class="sxs-lookup"><span data-stu-id="1e037-118">This form must be installed as a fully trusted form to run.</span></span> <span data-ttu-id="1e037-119">Para obtener información acerca de cómo depurar una plantilla de formulario de plena confianza, vea [obtener una vista previa y depurar plantillas de formulario que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="1e037-119">For information on debugging a fully trusted form template, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> <span data-ttu-id="1e037-120">Para obtener información sobre la implementación de una plantilla de formulario de plena confianza, vea [Implementar plantillas de formulario de InfoPath con código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="1e037-120">For information on deploying a fully trusted form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
  
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
    [InfoPathNamespace("xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
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



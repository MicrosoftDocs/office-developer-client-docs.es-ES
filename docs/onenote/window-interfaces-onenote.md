---
title: Interfaces de ventana (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Las interfaces de ventana y Windows son que objetos de OneNote 2013 API que permite a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.
ms.openlocfilehash: 83a3742419a4c8faf11c22c4766744d675151c1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816056"
---
# <a name="window-interfaces-onenote"></a>Interfaces de ventana (OneNote)

Las interfaces de **ventana** y **Windows** son que objetos de OneNote 2013 API que permite a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana. 
  
## <a name="onenote-window-views"></a>Vistas de ventana de OneNote

En la siguiente lista se muestra los modos de cuatro vistas que pueden usar para ventanas de OneNote: 
  
- La vista normal: muestra la ventana de OneNote predeterminado en el que los paneles de navegación del Bloc de notas y página están visibles.
    
- Vista de página completa: muestra la vista de una mínimo de interfaz de usuario (UI) en que no se muestran los paneles de Bloc de notas y página.
    
- Nota rápida: muestra una pequeña ventana que permite a los usuarios tomar notas breves. Normalmente, podría tener acceso a notas rápidas mediante el icono de OneNote en el área de notificación de Windows, pero también se pueden tener acceso a ellas a través de la ficha **Ver** en OneNote. 
    
- Acople al escritorio: muestra una ventana de OneNote que se puede acoplar a cualquier lado del escritorio (similar a la barra de tareas). Esta vista reduce el tamaño del escritorio para ajustarlo a la ventana. Sólo una ventana se puede acoplar en cualquier momento, y la ventana está siempre visible sin bloquear el escritorio. 
    
La siguiente ilustración muestra qué la vista de página completa, vista del escritorio, el tránsito y notas rápidas de aspecto en el escritorio.
  
**Vistas de OneNote**

![Vistas de la ventana de OneNote] (media/ON15Con_views.jpg "Vistas de la ventana de OneNote")
  
## <a name="interfaces"></a>Interfaces

En esta sección se enumera las interfaces y miembros que se pueden utilizar para modificar ventanas de OneNote mediante programación.
  
### <a name="windows-interface"></a>Interfaz de Windows

La interfaz de **Windows** permite al usuario tener acceso al conjunto de ventanas abiertas de OneNote. Es una propiedad de la clase de **aplicación** de OneNote, tiene acceso a través de **Application.Windows**. Esto devuelve el conjunto enumerado de ventanas de OneNote. 
  
**Propiedades**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Obtiene el número de objetos de **ventana** en el conjunto de **Windows** .  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Obtiene el objeto de **ventana** de la ventana activa de OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Devuelve el objeto de **ventana** que corresponde al valor de índice que se pasa. Esta propiedad no se puede tener acceso directamente. Para devolver un objeto **Window** , use **Windows [(uint) índice]**.  <br/> |
   
### <a name="window-interface"></a>Interfaz de ventana

La interfaz de **ventana** permite al usuario tener acceso a determinadas propiedades de cada ventana. Para obtener acceso a cada ventana de OneNote enumerar a través de la propiedad de **Windows** de la clase de **aplicación** . 
  
**Propiedades**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es la ventana activa de OneNote.  <br/> |
|**Aplicación** <br/> |**Aplicación** <br/> |Obtiene el objeto de **aplicación** de OneNote que está asociado a la ventana.  <br/> |
|**CurrentPageId** <br/> |cadena  <br/> |Obtiene el identificador del objeto de la página activa de OneNote de la ventana.  <br/> |
|**CurrentSectionId** <br/> |cadena  <br/> |Obtiene el identificador del objeto de la sección activa de OneNote de la ventana.  <br/> |
|**CurrentSectionGroupId** <br/> |cadena  <br/> |Obtiene el identificador de objeto del grupo de sección de OneNote activo de la ventana.  <br/> |
|**CurrentNotebookId** <br/> |cadena  <br/> |Obtiene el identificador de objeto del Bloc de notas de OneNote activo de la ventana.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Obtiene o establece la ubicación acoplada de la ventana de OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana está en vista de página completa (vista mínima de la interfaz de usuario).  <br/> |
|**Nota al margen** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es una ventana de nota rápida.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador del controlador de la ventana de OneNote.  <br/> |
   
**Métodos**
  
Puede usar los siguientes métodos de la interfaz de **ventana** para navegar a los objetos especificados en la ventana de OneNote o a las direcciones URL especificadas. 
  
**DesplazarseA**

|||
|:-----|:-----|
|**Descripción** <br/> |Se desplaza al objeto especificado en la ventana de OneNote. Por ejemplo, puede navegar a secciones, páginas y elementos de esquema dentro de las páginas.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parameters** <br/> | _bstrHierarchyObjectID_: la jerarquía de OneNote identificador del objeto que va a explorar a. El identificador de objeto puede hacer referencia a un bloc de notas de OneNote, sección, grupo de sección o página.  <br/>  _bstrObjectID_: el identificador de OneNote del objeto específico al que navegar dentro de una página de OneNote. Si no desea que el usuario navegar a un objeto específico en una página, este parámetro se establece en null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Descripción** <br/> |Si pasa un vínculo de OneNote (onenote: / /), se abre la ventana de OneNote a la ubicación correspondiente en OneNote. Sin embargo, si el vínculo es un vínculo externo, por ejemplo, http:// o file://, aparecerá un cuadro de diálogo de seguridad. Tras despido, OneNote intenta abrir el vínculo y se devuelve un error de HResult.hrObjectDoesNotExist.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parameters** <br/> | _bstrUrl_: la dirección URL de destino.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Descripción** <br/> |La ventana se acopla a la ubicación especificada por el monitor en **ptMonitor**y **dockLocation** .  <br/> |
|**Sintaxis** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parameters** <br/> | _dockLocation_ - indica la ubicación de una ventana de OneNote 2013 acoplada.  <br/>  _ptMonitor_ - indica (opcional) en x, y de coordenadas que supervisar la ventana debe se puede acoplar a.  <br/> |
   
## <a name="example"></a>Ejemplo

El siguiente código recorre en iteración las ventanas de OneNote para buscar una ventana acoplada. Si no existe ninguna ventana acoplada, en el ejemplo se acopla a la ventana activa. Si no existe ninguna ventana activa, el código crea una nueva ventana acoplada.
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a>Ver también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)


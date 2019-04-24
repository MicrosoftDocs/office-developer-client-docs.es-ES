---
title: Interfaces de ventana (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Las interfaces Window y Windows son objetos de la API de OneNote 2013 que permiten a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317041"
---
# <a name="window-interfaces-onenote"></a>Interfaces de ventana (OneNote)

Las interfaces **Window** y **Windows** son objetos de la API de OneNote 2013 que permiten a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana. 
  
## <a name="onenote-window-views"></a>Vistas de ventana de OneNote

La siguiente lista muestra los cuatro modos de vista que puede usar en las ventanas de OneNote: 
  
- Vista normal: muestra la ventana de OneNote predeterminada en la que se ven los paneles de navegación del Bloc de notas y de la página.
    
- Vista página completa: muestra una vista de interfaz de usuario mínima (UI) en la que no se muestran los paneles de Bloc de notas y de página.
    
- Nota rápida: muestra una pequeña ventana que permite a los usuarios tomar notas cortas. Normalmente, tendría acceso a las notas rápidas a través del icono de OneNote en el área de notificación de Windows, pero también puede tener acceso a ellas a través de la pestaña **Ver** de OneNote. 
    
- Acoplar al escritorio: muestra una ventana de OneNote que puede acoplar a cualquier lado del escritorio (similar a la barra de tareas). Esta vista reduce el tamaño del escritorio para ajustarlo a la ventana. Puede acoplar solo una ventana en cualquier momento y la ventana siempre está visible sin bloquear el escritorio. 
    
En la siguiente figura se muestra el aspecto de la vista de página completa, la vista acoplada al escritorio y las notas rápidas en el escritorio.
  
**Vistas de OneNote**

![Vistas de ventana de OneNote] (media/ON15Con_views.jpg "Vistas de ventana de OneNote")
  
## <a name="interfaces"></a>Interfaces

En esta sección se enumeran las interfaces y los miembros que se pueden usar para modificar las ventanas de OneNote mediante programación.
  
### <a name="windows-interface"></a>Interfaz de Windows

La interfaz de **Windows** permite al usuario tener acceso al conjunto de ventanas de OneNote abiertas. Se trata de una propiedad de la clase de la **aplicación** de OneNote, a la que se tiene acceso a través de **Application. Windows**. Esto devuelve el conjunto enumerado de ventanas de OneNote. 
  
**Properties**

|**Name**|**Type**|**Descripción**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Obtiene el número de objetos de **ventana** en el conjunto de **ventanas** .  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Obtiene el objeto **Window** de la ventana activa de OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Devuelve el objeto **Window** que corresponde al valor de índice pasado. No se puede obtener acceso a esta propiedad directamente. Para devolver un objeto **Window** , use **Windows [(uint) index]**.  <br/> |
   
### <a name="window-interface"></a>Interfaz de ventana

La interfaz de **ventana** permite al usuario tener acceso a determinadas propiedades de cada ventana. Se puede tener acceso a cada ventana de OneNote mediante la enumeración de la propiedad **Windows** de la clase **Application** . 
  
**Properties**

|**Name**|**Type**|**Descripción**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es la ventana activa de OneNote.  <br/> |
|**Application** <br/> |**Application** <br/> |Obtiene el objeto de la **aplicación** de OneNote que está asociado a la ventana.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Obtiene el identificador de objeto de la página de OneNote activa de la ventana.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Obtiene el identificador de objeto de la sección de OneNote activa de la ventana.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Obtiene el identificador de objeto del grupo de secciones de OneNote activo de la ventana.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Obtiene el identificador de objeto del Bloc de notas de OneNote activo de la ventana.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Obtiene o establece la ubicación acoplada de la ventana de OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana está en vista de página completa (vista de la interfaz de usuario mínima).  <br/> |
|**SideNote** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es una ventana de nota rápida.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador de identificador de la ventana de OneNote.  <br/> |
   
**Métodos**
  
Puede usar los siguientes métodos de la interfaz de **ventana** para navegar a los objetos especificados en la ventana de OneNote o a las direcciones URL especificadas. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Descripción** <br/> |Se desplaza al objeto especificado en la ventana de OneNote. Por ejemplo, puede desplazarse a secciones, páginas y elementos de esquema dentro de las páginas.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parámetros** <br/> | _bstrHierarchyObjectID_: el identificador de OneNote de la jerarquía del objeto al que desea desplazarse. El identificador de objeto puede hacer referencia a un bloc de notas, sección, grupo de secciones o página de OneNote.  <br/>  _bstrObjectID_: el identificador de OneNote del objeto específico al que navegar en una página de OneNote. Si el usuario no desea desplazarse a un objeto específico de una página, este parámetro se establece en NULL.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Descripción** <br/> |Si se pasó un vínculo de OneNote (onenote://), se abrirá la ventana de OneNote en la ubicación correspondiente en OneNote. Sin embargo, si el vínculo es un vínculo externo, como https://o file://, aparecerá un cuadro de diálogo de seguridad. Tras el descarte, OneNote intenta abrir el vínculo y se devuelve un error HResult. hrObjectDoesNotExist.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parámetros** <br/> | _bstrUrl_: dirección URL a la que desplazarse.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Descripción** <br/> |Acopla la ventana a la ubicación especificada por **dockLocation** y el monitor a **ptMonitor**.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parámetros** <br/> | _dockLocation_ : indica la ubicación acoplada de una ventana de 2013 de OneNote.  <br/>  _ptMonitor_ : (opcional) indica las coordenadas x, y que supervisan la ventana a la que se debe acoplar.  <br/> |
   
## <a name="example"></a>Ejemplo

El código siguiente recorre en iteración las ventanas de OneNote para buscar una ventana acoplada. Si no existe ninguna ventana acoplada, el ejemplo acopla la ventana activa. Si no existe ninguna ventana activa, el código crea una nueva ventana acoplada.
  
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


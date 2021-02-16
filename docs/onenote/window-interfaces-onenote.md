---
title: Interfaces de ventana (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Las interfaces de Windows y Windows son objetos de la API de OneNote 2013 que permiten a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317041"
---
# <a name="window-interfaces-onenote"></a>Interfaces de ventana (OneNote)

Las **interfaces** **de Windows** y Windows son objetos de la API de OneNote 2013 que permiten a los usuarios trabajar con ventanas de OneNote. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana. 
  
## <a name="onenote-window-views"></a>Vistas de ventana de OneNote

En la siguiente lista se muestran los cuatro modos de vista que puede usar para las ventanas de OneNote: 
  
- Vista normal: muestra la ventana predeterminada de OneNote en la que están visibles los paneles de navegación Bloc de notas y Página.
    
- Vista página completa: muestra una vista de interfaz de usuario (UI) mínima en la que no se muestran los paneles Bloc de notas y Página.
    
- Nota rápida: muestra una ventana pequeña que permite a los usuarios tomar notas breves. Normalmente, accedería a notas rápidas a través del icono de OneNote en el área de notificación de Windows, pero también puede acceder a ellas a través de la pestaña **Ver** en OneNote. 
    
- Acoplar a escritorio: muestra una ventana de OneNote que puede acoplar a cualquier lado del escritorio (similar a la barra de tareas). Esta vista reduce el tamaño del escritorio para ajustarse a la ventana. Solo se puede acoplar una ventana en cualquier momento y la ventana siempre es visible sin bloquear el escritorio. 
    
En la figura siguiente se muestra el aspecto de la vista Página completa, la vista Acoplar a escritorio y las notas rápidas en el escritorio.
  
**Vistas de OneNote**

![Vistas de ventana de OneNote vistas](media/ON15Con_views.jpg "de ventana de OneNote")
  
## <a name="interfaces"></a>Interfaces

En esta sección se enumeran las interfaces y los miembros que puede usar para modificar las ventanas de OneNote mediante programación.
  
### <a name="windows-interface"></a>Interfaz de Windows

La interfaz de **Windows** permite al usuario tener acceso al conjunto de ventanas de OneNote abiertas. Es una propiedad de la clase **Application de** OneNote, a la que se tiene acceso a través **de Application.Windows**. Devuelve el conjunto enumerado de ventanas de OneNote. 
  
**Properties**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Obtiene el número de **objetos Window** del conjunto **de Windows.**  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Obtiene el **objeto Window** de la ventana activa de OneNote.  <br/> |
|**Items** <br/> |**Window** <br/> |Devuelve el **objeto Window** que corresponde al valor de índice pasado. No se puede tener acceso a esta propiedad directamente. Para devolver un **objeto Window,** utilice **windows [(uint) índice]**.  <br/> |
   
### <a name="window-interface"></a>Interfaz de ventana

La **interfaz window** permite al usuario tener acceso a determinadas propiedades de cada ventana. Se puede tener acceso a cada ventana de OneNote enumerando a través de la propiedad **Windows** de la **clase Application.** 
  
**Properties**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es la ventana activa de OneNote.  <br/> |
|**Application** <br/> |**Application** <br/> |Obtiene el objeto **Application de** OneNote asociado a la ventana.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Obtiene el identificador de objeto de la página activa de OneNote de la ventana.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Obtiene el identificador de objeto de la sección activa de OneNote de la ventana.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Obtiene el identificador de objeto del grupo de secciones de OneNote activo de la ventana.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Obtiene el identificador de objeto del bloc de notas de OneNote activo de la ventana.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Obtiene o establece la ubicación acoplada de la ventana de OneNote.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana está en la vista Página completa (vista de interfaz de usuario mínima).  <br/> |
|**SideNote** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es una ventana de nota rápida.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador de identificador de la ventana de OneNote.  <br/> |
   
**Métodos**
  
Puede usar los siguientes métodos de la interfaz **window** para navegar a objetos especificados en la ventana de OneNote o a direcciones URL especificadas. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Descripción** <br/> |Navega al objeto especificado en la ventana de OneNote. Por ejemplo, puede navegar a secciones, páginas y elementos de esquema dentro de las páginas.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parámetros** <br/> | _bstrHierarchyObjectID:_ id. de OneNote de jerarquía del objeto al que quieres navegar. El identificador de objeto puede hacer referencia a un bloc de notas, una sección, un grupo de secciones o una página de OneNote.  <br/>  _bstrObjectID:_ id. de OneNote del objeto específico al que navegar dentro de una página de OneNote. Si el usuario no desea navegar a un objeto específico de una página, este parámetro se establece en null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Descripción** <br/> |Si se pasó un vínculo de OneNote (onenote://), se abrirá la ventana de OneNote en la ubicación correspondiente en OneNote. Sin embargo, si el vínculo es un vínculo externo, como https:// o file://, aparecerá un cuadro de diálogo de seguridad. Tras el rechazo, OneNote intenta abrir el vínculo y se devuelve un error HResult.hrObjectDoesNotExist.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parámetros** <br/> | _bstrUrl:_ dirección URL a la que navegar.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Descripción** <br/> |Acopla la ventana a la ubicación especificada por **dockLocation** y el monitor en **ptMonitor**.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parámetros** <br/> | _dockLocation:_ indica la ubicación acoplada de una ventana de OneNote 2013.  <br/>  _ptMonitor:_ (opcional) indica en coordenadas x,y a las que se debe acoplar la ventana.  <br/> |
   
## <a name="example"></a>Ejemplo

El siguiente código recorre en iteración las ventanas de OneNote para encontrar una ventana acoplada. Si no existe ninguna ventana acoplada, el ejemplo acopla la ventana activa. Si no existe ninguna ventana activa, el código crea una nueva ventana acoplada.
  
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


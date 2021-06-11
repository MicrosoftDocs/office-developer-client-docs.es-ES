---
title: Interfaces de ventana (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Las interfaces Window y Windows son OneNote api de 2013 que permite a los usuarios trabajar con OneNote windows. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317041"
---
# <a name="window-interfaces-onenote"></a>Interfaces de ventana (OneNote)

Las **interfaces Window** **y Windows** son OneNote api de 2013 que permite a los usuarios trabajar con OneNote windows. Estos objetos permiten a los usuarios enumerar a través del conjunto de ventanas de OneNote y modificar determinadas propiedades de la ventana. 
  
## <a name="onenote-window-views"></a>Vistas de ventana de OneNote

En la lista siguiente se muestran los cuatro modos de vista que se pueden usar para OneNote ventanas: 
  
- Vista normal: muestra la ventana OneNote predeterminada en la que están visibles los paneles de navegación Bloc de notas y Página.
    
- Vista Página completa: muestra una vista de interfaz de usuario (UI) mínima en la que no se muestran los paneles Bloc de notas y Página.
    
- Nota rápida: muestra una pequeña ventana que permite a los usuarios tomar notas breves. Normalmente, accedería a notas rápidas a través del icono OneNote en el área de  notificación de Windows, pero también puede acceder a ellas a través de la pestaña Ver en OneNote. 
    
- Acoplar a escritorio: muestra una OneNote que puede acoplar a cualquier lado del escritorio (similar a la barra de tareas). Esta vista reduce el tamaño del escritorio para que se ajuste a la ventana. Solo puede acoplar una ventana en cualquier momento y la ventana siempre está visible sin bloquear el escritorio. 
    
En la siguiente figura se muestra el aspecto de la vista Página completa, la vista Acoplar a escritorio y las notas rápidas en el escritorio.
  
**Vistas de OneNote**

![OneNote vistas de ventana OneNote]vistas de(media/ON15Con_views.jpg "ventana")
  
## <a name="interfaces"></a>Interfaces

En esta sección se enumeran las interfaces y los miembros que puede usar para modificar las OneNote mediante programación.
  
### <a name="windows-interface"></a>Windows interfaz

La **Windows** permite al usuario tener acceso al conjunto de ventanas OneNote abiertas. Es una propiedad de la clase OneNote **Application,** a la que se accede a través **de Application.Windows**. Esto devuelve el conjunto enumerado de OneNote ventanas. 
  
**Properties**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Count** <br/> |ulong  <br/> |Obtiene el número de **objetos Window** del **Windows** conjunto.  <br/> |
|**CurrentWindow** <br/> |**Window** <br/> |Obtiene el **objeto Window** de la ventana OneNote activa.  <br/> |
|**Items** <br/> |**Window** <br/> |Devuelve el **objeto Window** que corresponde al valor de índice pasado. No se puede tener acceso a esta propiedad directamente. Para devolver un **objeto Window,** use **Windows [(uint) index]**.  <br/> |
   
### <a name="window-interface"></a>Interfaz de ventana

La **interfaz Window** permite al usuario tener acceso a determinadas propiedades de cada ventana. Cada OneNote puede tener acceso enumerando a través de la **Windows** propiedad de la **clase Application.** 
  
**Properties**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Active** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es la ventana OneNote activa.  <br/> |
|**Application** <br/> |**Application** <br/> |Obtiene el OneNote **application** asociado a la ventana.  <br/> |
|**CurrentPageId** <br/> |string  <br/> |Obtiene el identificador de objeto de la página OneNote activa de la ventana.  <br/> |
|**CurrentSectionId** <br/> |string  <br/> |Obtiene el identificador de objeto de la OneNote de la ventana.  <br/> |
|**CurrentSectionGroupId** <br/> |string  <br/> |Obtiene el identificador de objeto del grupo de OneNote de sección activo de la ventana.  <br/> |
|**CurrentNotebookId** <br/> |string  <br/> |Obtiene el identificador de objeto del bloc de notas OneNote activo de la ventana.  <br/> |
|**DockedLocation** <br/> |**DockedLocation** <br/> |Obtiene o establece la ubicación acoplada de la OneNote ventana.  <br/> |
|**FullPageView** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana está en la vista Página completa (vista de interfaz de usuario mínima).  <br/> |
|**SideNote** <br/> |bool  <br/> |Obtiene o establece un valor que indica si la ventana es una ventana de nota rápida.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador de identificador de la OneNote ventana.  <br/> |
   
**Métodos**
  
Puede usar los siguientes métodos de la interfaz **Window** para navegar a objetos especificados en la ventana OneNote o a direcciones URL especificadas. 
  
**NavigateTo**

|||
|:-----|:-----|
|**Descripción** <br/> |Navega hasta el objeto especificado en la OneNote ventana. Por ejemplo, puede navegar a secciones, páginas y elementos de esquema dentro de las páginas.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); ` <br/> |
|**Parámetros** <br/> | _bstrHierarchyObjectID:_ la jerarquía OneNote identificador del objeto al que desea navegar. El identificador de objeto puede hacer referencia a OneNote bloc de notas, sección, grupo de secciones o página.  <br/>  _bstrObjectID:_ el OneNote identificador del objeto específico al que se va a navegar dentro de una OneNote página. Si el usuario no desea navegar a un objeto específico de una página, este parámetro se establece en null.  <br/> |
   
**NavigateToUrl**

|||
|:-----|:-----|
|**Descripción** <br/> |Si se pasó un vínculo de OneNote (onenote://), se abrirá la ventana de OneNote en la ubicación correspondiente en OneNote. Sin embargo, si el vínculo es un vínculo externo, como https:// o file://, aparecerá un cuadro de diálogo de seguridad. Tras el despido, OneNote intenta abrir el vínculo y se devuelve un error HResult.hrObjectDoesNotExist.  <br/> |
|**Sintaxis** <br/> | `HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); ` <br/> |
|**Parámetros** <br/> | _bstrUrl:_ la dirección URL a la que se va a navegar.  <br/> |
   
**SetDockedLocation**

|||
|:-----|:-----|
|**Descripción** <br/> |Acopla la ventana a la ubicación especificada por **dockLocation** y el monitor en **ptMonitor**.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);` <br/> |
|**Parámetros** <br/> | _dockLocation:_ indica la ubicación acoplada de una OneNote 2013.  <br/>  _ptMonitor:_ (opcional) Indica en las coordenadas x,y a las que se debe acoplar la ventana.  <br/> |
   
## <a name="example"></a>Ejemplo

El siguiente código recorre en iteración las ventanas OneNote para buscar una ventana acoplada. Si no existe ninguna ventana acoplada, el ejemplo acopla la ventana activa. Si no existe ninguna ventana activa, el código crea una nueva ventana acoplada.
  
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


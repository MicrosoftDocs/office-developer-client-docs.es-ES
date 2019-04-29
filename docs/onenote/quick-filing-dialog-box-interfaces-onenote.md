---
title: Interfaces del cuadro de diálogo de archivado rápido (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: En este tema se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo de archivado rápido en OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425340"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Interfaces del cuadro de diálogo de archivado rápido (OneNote)

En este tema se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo de archivado rápido en OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Cuadro de diálogo de archivado rápido

El cuadro de diálogo de archivado rápido de OneNote 2013 es un cuadro de diálogo personalizable que permite a los usuarios seleccionar una ubicación dentro de la estructura jerárquica de OneNote. Las ubicaciones seleccionables incluyen los blocs de notas, grupos de secciones, secciones, páginas y subpáginas. El cuadro de diálogo se usa tanto en la aplicación de OneNote como mediante aplicaciones externas a través de la API 2013 de OneNote. La figura 1 muestra el cuadro de diálogo de archivado rápido en su estado predeterminado.
  
**Figura 1. Cuadro de diálogo de archivado rápido sin personalizaciones**

![Cuadro de diálogo de archivaDo rápido sin personalizaciones] (media/ON15Con_quick_filing_dialog.jpg "Cuadro de diálogo de archivaDo rápido sin personalizaciones")
  
En el cuadro de diálogo, los usuarios pueden desplazarse por la jerarquía de todos los blocs de notas para buscar ubicaciones específicas o buscar en la estructura de árbol de OneNote escribiendo en el cuadro de texto. Algunos aspectos del cuadro de diálogo que se pueden personalizar son el título, la descripción, la lista de resultados recientes, el texto y el estado de las casillas de verificación, la profundidad del árbol, los botones y los tipos de ubicaciones seleccionables.

Puede tener acceso a la funcionalidad del cuadro de diálogo de archivado rápido a través de dos interfaces de OneNote 2013. La interfaz **IQuickFilingDialog** permite a los usuarios crear instancias, configurar y ejecutar el cuadro de diálogo. Se llama a la interfaz **IQuickFilingDialogCallback** después de cerrar el cuadro de diálogo. El cuadro de diálogo se ejecuta en el proceso de OneNote, por lo que se necesita un mecanismo para mantener el subproceso del cuadro de diálogo en ejecución y, a continuación, para capturar la selección del usuario y el estado del cuadro de diálogo cuando se cierra. 
  
## <a name="iquickfilingdialog-interface"></a>Interfaz IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Esta interfaz permite al usuario personalizar y ejecutar el cuadro de diálogo. El usuario puede crear una instancia de un cuadro de diálogo a través de la clase **Application** mediante el método **Application. QuickFilingDialog** . El método devuelve una instancia del cuadro de diálogo. Una vez que se establecen las propiedades del cuadro de diálogo, se usa el método **IQuickFilingDialog. Run** para ejecutar el cuadro de diálogo. Este método ejecuta el cuadro de diálogo en un nuevo subproceso. 
  
**Properties**

|**Name**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Title** <br/> |cadena  <br/> |Obtiene o establece el texto del título que aparece en la barra de título de la ventana de cuadro de diálogo.  <br/> |
|**Descripción** <br/> |cadena  <br/> |Obtiene o establece la descripción del texto para indicar al usuario qué debe seleccionar. Este valor puede ser texto de varias líneas.  <br/> |
|**CheckboxText** <br/> |cadena  <br/> |Obtiene o establece el texto que sigue a la casilla de verificación. Si este valor se establece en una cadena no vacía, aparecerá una casilla de verificación en el cuadro de diálogo. Si el valor es una cadena vacía, no aparece ninguna casilla de verificación.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Obtiene o establece el estado de la casilla de verificación. Si el valor se establece en **false**, la casilla de verificación se desactiva al iniciar el cuadro de diálogo. Si el valor se establece en **true**, la casilla de verificación se activa cuando se inicia el cuadro de diálogo, siempre y cuando **CheckboxText** sea una cadena no vacía.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador del identificador de la ventana del cuadro de diálogo de archivado rápido.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Obtiene o establece la profundidad que debe mostrarse el árbol de OneNote en la sección todos los blocs de notas. De forma predeterminada, el árbol se muestra en las secciones. Esta propiedad no afecta al tipo de elementos que se pueden seleccionar.  <br/> Si **TreeDepth** se establece en un elemento inferior de la jerarquía de OneNote del que puede ser seleccionado por cualquiera de los botones, la profundidad del árbol mostrado será el menor posible elemento seleccionable. Es decir, si se establece la profundidad de árbol para mostrar las páginas hacia abajo, pero el menor elemento seleccionable es una sección, el árbol se muestra en las secciones.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Obtiene o establece el identificador del identificador de la ventana principal del cuadro de diálogo. Si se establece esta propiedad, el cuadro de diálogo de archivado rápido será modal en la ventana primaria asignada cuando se abra el cuadro de diálogo. Es decir, un usuario no podrá obtener acceso a la ventana primaria hasta que se cierre el cuadro de diálogo de archivado rápido.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Obtiene o establece la posición de la ventana con relación a la pantalla. De forma predeterminada, el cuadro de diálogo aparece en la parte central de la ventana principal o en el escritorio.  <br/> |
|**SelectedItem** <br/> |cadena  <br/> |Obtiene el identificador de objeto de la ubicación de OneNote seleccionada por el usuario cuando se cierra el cuadro de diálogo. Si el usuario hace clic en el botón **Cancelar** , el objeto se establece en NULL.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Obtiene el botón en el que se hizo clic cuando se cerró el cuadro de diálogo. Si se hizo clic en el botón **Cancelar** , esta propiedad devuelve un valor de-1. A todos los demás botones se les asignan valores enteros de 0, que se incrementan en 1 para cada botón agregado al cuadro de diálogo. El valor entero del botón **Aceptar** predeterminado es 0.  <br/> |
   
### <a name="methods"></a>Métodos

**SetRecentResults**

|||
|:-----|:-----|
|**Descripción** <br/> |Establece la lista de resultados recientes que se mostrará en el cuadro de diálogo de archivado rápido e indica si se deben incluir ubicaciones de archivos especiales en la lista. Los usuarios pueden seleccionar una lista de resultados recientes de la enumeración [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Los usuarios también pueden elegir agregar las siguientes opciones a la lista: sección actual, página actual o notas no archivadas. Si se selecciona **RecentResultType. rrtNone** , no se muestra ninguna lista de resultados recientes.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Parámetros** <br/> | _recentResults_ &ndash; Un objeto de tipo **RecentResultType** que indica qué lista de resultados recientes, si la hay, debe aparecer. Si se selecciona **rrtNone** , no aparece ninguna lista de resultados recientes en el cuadro de diálogo.<br/><br/>  _fShowCurrentSection_ &ndash; Un valor booleano que indica si la sección actual debe incluirse en la lista de resultados recientes.<br/><br/>  _fShowCurrentPage_ &ndash; Un valor booleano que indica si la página actual debe incluirse en la lista de resultados recientes.<br/><br/>  _fShowUnfiledNotes_ &ndash; Un valor booleano que indica si la sección Notas no archivadas debe incluirse en la lista de resultados recientes.  <br/> |
   
> [!NOTE]
> Si no se puede seleccionar una ubicación de archivado especial mediante cualquiera de los botones del cuadro de diálogo, no se muestra en la lista. Si no se encuentra un elemento seleccionable en la lista de resultados recientes, no se muestra ninguna lista de resultados recientes. 
  
El siguiente ejemplo usa el método **SetRecentResults** para mostrar la sección actual, la página actual y la sección Notas no archivadas en la lista de resultados recientes. 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

**AddButton**

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios agregar y personalizar botones en el cuadro de diálogo. Los usuarios pueden especificar el texto de los botones y los elementos de la jerarquía de OneNote que puede seleccionar cada botón.  <br/> |
|**Sintaxis** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Parámetros** <br/> | _bstrText_ &ndash; Una cadena que especifica el texto que va a aparecer en el botón. Para personalizar el botón **Aceptar** predeterminado, pase un valor nulo como **bstrText**.  <br/><br/>_allowedElements_ &ndash; Un **HierarchyElement** que indica qué elementos de la jerarquía de OneNote que no son de solo lectura puede seleccionar un usuario mediante el botón. Para seleccionar varios elementos, el usuario debe pasar el operador **or** para todos los valores equivalentes de uint de los tipos de **HierarchyElement** permitidos como **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_ &ndash; **HierarchyElement** que indica qué elementos de la jerarquía de solo lectura de OneNote puede seleccionar un usuario mediante el botón. Para seleccionar varios elementos, el usuario debe pasar el operador **or** para todos los valores de los equivalentes de **uint** de los tipos de **HierarchyElement** permitidos como **HierarchyElement**.<br/><br/>  _fDefault_ &ndash; Un valor booleano que especifica si este botón debe ser el botón predeterminado. Si se establecen varios botones como predeterminados, el último botón especificado se convierte en el botón predeterminado.  <br/> |
   
En el ejemplo siguiente se agregan tres botones al cuadro de diálogo de archivado rápido. El primero de ellos **** puede seleccionarse por todos los elementos del árbol de jerarquía de OneNote. El resto, los blocs de **notas** y **las páginas**solo se pueden seleccionar si se seleccionan sus elementos, blocs de notas y páginas correspondientes.
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

**Run**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra el cuadro de diálogo de archivado rápido de un nuevo hilo. Toma una referencia a la interfaz **IQuickFilingDialogCallback** , cuyo método **OnDialogClosed** se llamará una vez que se cierre el cuadro de diálogo.  <br/> |
|**Sintaxis** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Parámetros** <br/> | _piCallback_ &ndash; Una referencia a la interfaz de **IQuickFilingDialogCallback** que se creará una vez que se cerrará el cuadro de diálogo.  <br/> |
   
En el ejemplo siguiente se usa el método **Run** para mostrar el cuadro de diálogo de archivado rápido de un nuevo hilo. 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

**TreeCollapsedState**

|||
|:-----|:-----|
|**Descripción** <br/> |Indica si el árbol de jerarquía se debe expandir o contraer.  <br/> |
|**Sintaxis** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Parámetros** <br/> | _ect_ : especifica si el árbol está expandido o contraído.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Descripción** <br/> |Filtra la lista de blocs de notas que se muestran por tipo.  <br/> |
|**Sintaxis** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Parámetros** <br/> | _NFO_ -especifica el conjunto de blocs de notas que se van a filtrar de la lista  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra la opción Crear nuevo Bloc de notas en el cuadro de diálogo.  <br/> |
|**Sintaxis** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Parámetros** <br/> |Ninguna  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Descripción** <br/> |Agrega un usuario como un editor inicial a un bloc de notas en el cuadro de diálogo de archivado rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Parámetros** <br/> | _initialEditor_ : la dirección de correo electrónico del usuario que desea agregar como editor al bloc de notas. Cuando se crea el Bloc de notas mediante el cuadro de diálogo de archivado rápido, se comparte automáticamente con todos los editores iniciales.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Descripción** <br/> |Quita todos los editores iniciales del cuadro de diálogo de archivado rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Parámetros** <br/> |Ninguna  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra el hiperVínculo del tema de ayuda de uso compartido en el cuadro de diálogo de archivado rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Parámetros** <br/> |Ninguna  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Interfaz IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Esta interfaz permite al usuario tener acceso a las propiedades del cuadro de diálogo después de cerrar el cuadro de diálogo. Una vez que se cierra el cuadro de diálogo, OneNote 2013 llama al método **IQuickFilingDialogCallback. OnDialogClose** en esta interfaz. 
  
Debe definirse una clase que herede esta interfaz.
  
### <a name="methods"></a>Métodos

En la siguiente sección se describen los métodos asociados con las interfaces detalladas anteriormente.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios agregar funciones para capturar y usar la selección del usuario en el cuadro de diálogo. Se llama a este método después de cerrar el cuadro de diálogo de archivado rápido. Este método es una función que las interfaces de **IQuickFilingDialogCallback** tienen que definir.  <br/> |
|**Sintaxis** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Parámetros** <br/> | _cuadro de diálogo_ &ndash; El objeto **IQuickFilingDialog** que llamó al método **OnDialogClose** .  <br/> |
   
El siguiente ejemplo es una interfaz **IQuickFilingDialogCallback** de ejemplo. El método **OnDialogClose** imprime la selección del usuario desde el cuadro de diálogo de archivado rápido en la consola. 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a>Ejemplo
<a name="odc_IQuickFilingDialog"> </a>

En el ejemplo de código siguiente se abre un cuadro de diálogo de archivado rápido que tiene un título, una descripción, una lista de resultados recientes, una profundidad de árbol, una casilla de verificación y botones personalizados. El elemento seleccionado del usuario, el botón presionado y el estado de casilla se mostrarán en una ventana de consola cuando se cierre el cuadro de diálogo. Para ver el botón página habilitado, el usuario tendrá que buscar una página y seleccionarla, ya que la profundidad del árbol está configurada en secciones. El cuadro de diálogo no es un elemento secundario de ninguna ventana.
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a>Ver también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)


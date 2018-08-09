---
title: Interfaces de cuadro de diálogo de archivado rápidas (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: En este tema se describe las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo fiscal rápido en OneNote 2013.
ms.openlocfilehash: d2647ed4d7b9f4487c033260eba8df1e4281c6ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816046"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Interfaces de cuadro de diálogo de archivado rápidas (OneNote)

En este tema se describe las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo fiscal rápido en OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Cuadro de diálogo de archivado rápido

El cuadro de diálogo fiscal rápido en OneNote 2013 es un cuadro de diálogo personalizable que permite a los usuarios seleccionar una ubicación dentro de la estructura de la jerarquía de OneNote. Las ubicaciones seleccionables incluyen los blocs de notas, grupos de sección, secciones, páginas y subpáginas. El cuadro de diálogo se usa dentro de la aplicación de OneNote y por las aplicaciones externas a través de la API de OneNote 2013. La figura 1 muestra el cuadro de diálogo fiscal rápido en su estado predeterminado.
  
**En la figura 1. Cuadro de diálogo de archivado rápido sin personalizaciones**

![Cuadro de diálogo de archivado rápido sin personalizaciones] (media/ON15Con_quick_filing_dialog.jpg "Cuadro de diálogo de archivado rápido sin personalizaciones")
  
En el cuadro de diálogo, los usuarios pueden navegar por la jerarquía de todos los blocs de notas para buscar ubicaciones específicas o buscar la estructura de árbol de OneNote escribiendo en el cuadro de texto. Aspectos del cuadro de diálogo que se pueden personalizar incluyen el título, descripción, lista de resultados de recientes, texto de la casilla de verificación y estado, profundidad de árbol, botones y tipos de ubicación seleccionable.

Puede tener acceso a la funcionalidad de cuadro de diálogo de archivado rápido a través de dos interfaces de OneNote 2013. La interfaz de **IQuickFilingDialog** permite a los usuarios crear instancias, configurar y ejecuta el cuadro de diálogo. La interfaz de **IQuickFilingDialogCallback** se llama una vez que se cierra el cuadro de diálogo. El cuadro de diálogo se ejecuta en el proceso de OneNote, por lo que se necesita un mecanismo para mantener los subprocesos del cuadro de diálogo Ejecutar y, a continuación, para capturar la selección del usuario y el estado del cuadro de diálogo cuando éste se cierra. 
  
## <a name="iquickfilingdialog-interface"></a>Interfaz IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Esta interfaz permite al usuario personalizar y ejecutar el cuadro de diálogo. El usuario puede crear una instancia de un cuadro de diálogo a través de la clase de **aplicación** mediante el método **Application.QuickFilingDialog** . El método devuelve una instancia del cuadro de diálogo. Una vez que se establecen las propiedades del cuadro de diálogo, el método **IQuickFilingDialog.Run** se usa para ejecutar el cuadro de diálogo. Este método ejecuta el cuadro de diálogo en un nuevo subproceso. 
  
**Propiedades**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Obtiene o establece el texto del título que aparece en la barra de título de la ventana del cuadro de diálogo.  <br/> |
|**Descripción** <br/> |string  <br/> |Obtiene o establece la descripción de texto para indicar al usuario acerca de lo que seleccione. Este valor puede ser texto con varias líneas.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Obtiene o establece el texto que sigue a la casilla de verificación. Si este valor se establece en una cadena no vacía, aparece una casilla de verificación en el cuadro de diálogo. Si el valor es una cadena vacía, no aparece ningún cuadro de verificación.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Obtiene o establece el estado de la casilla de verificación. Si el valor se establece en **false**, la casilla de verificación está desactivada cuando se inicia el cuadro de diálogo. Si el valor se establece en **true**, se selecciona la casilla de verificación cuando el cuadro de diálogo se inicia mientras **CheckboxText** es una cadena no vacía.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador del controlador de la ventana de cuadro de diálogo de archivado rápido.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Obtiene o establece la profundidad, el árbol de OneNote debe mostrarse en la sección de todos los blocs de notas. De forma predeterminada, se muestra el árbol hasta las secciones. Esta propiedad no afecta a qué tipo de elementos que se puede seleccionar.  <br/> Si **TreeDepth** se establece en un elemento inferior en la jerarquía de OneNote que se puede seleccionar cualquiera de los botones, la profundidad de árbol que se muestra será el elemento seleccionable posible más bajo. Es decir, si se establece la profundidad de árbol para mostrar hacia abajo hasta las páginas, pero el elemento seleccionable más bajo es una sección, se muestra el árbol hacia abajo hasta secciones.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Obtiene o establece el identificador del controlador de la ventana principal del cuadro de diálogo. Si se establece esta propiedad, el cuadro de diálogo fiscal rápido será modal a la ventana primaria asignado cuando se abre el cuadro de diálogo. Es decir, un usuario no podrá tener acceso a la ventana principal hasta que se cierre el cuadro de diálogo de archivado rápido.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Obtiene o establece la posición de la ventana en relación con la pantalla. De forma predeterminada, el cuadro de diálogo aparece en medio de la ventana principal o el escritorio.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Obtiene el identificador del objeto de la ubicación de OneNote seleccionado por el usuario cuando se cierra el cuadro de diálogo. Si el usuario hace clic en el botón **Cancelar** , el objeto se establece en null.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Obtiene qué botón se hizo clic cuando se ha cerrado el cuadro de diálogo. Si se ha hecho clic en el botón **Cancelar** , esta propiedad devuelve un valor de -1. Todos los otros botones se asignan valores enteros del 0, incrementada en 1 para cada botón que agregó en el cuadro de diálogo. El valor de número entero del botón **Aceptar** predeterminado es 0.  <br/> |
   
### <a name="methods"></a>Métodos

**SetRecentResults**

|||
|:-----|:-----|
|**Descripción** <br/> |Establece qué lista resultado recientes se mostrará en el cuadro de diálogo fiscal rápido e indica si se incluyen algunas ubicaciones de presentación especial en la lista. Los usuarios pueden seleccionar una lista de resultados recientes de la enumeración [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) . Los usuarios también pueden elegir agregar las siguientes opciones a la lista: sección actual, la página actual o notas sin archivar. Si se selecciona **RecentResultType.rrtNone** , no se muestra ninguna lista de resultados recientes.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Parameters** <br/> | _recentResults_ &ndash; Un objeto de tipo **RecentResultType** que indica qué lista resultado reciente, si lo hay, debe aparecer. Si se selecciona **rrtNone** , no aparecerá ninguna lista de resultados recientes en el cuadro de diálogo.<br/><br/>  _fShowCurrentSection_ &ndash; Valor de tipo Boolean que indica si la sección actual debe estar incluida en la lista de resultados recientes.<br/><br/>  _fShowCurrentPage_ &ndash; Valor de tipo Boolean que indica si la página actual debe estar incluida en la lista de resultados recientes.<br/><br/>  _fShowUnfiledNotes_ &ndash; Valor de tipo Boolean que indica si la sección Notas sin archivar debe estar incluida en la lista de resultados recientes.  <br/> |
   
> [!NOTE]
> Si no se puede seleccionar una ubicación de archivado especiales mediante cualquiera de los botones en el cuadro de diálogo, no se muestra en la lista. Si no hay ningún elemento seleccionable en la lista de resultados recientes se encuentra, no se muestra ninguna lista de resultados recientes. 
  
En el siguiente ejemplo, se utiliza el método **SetRecentResults** para mostrar la sección actual, la página actual y la sección Notas sin archivar en la lista de resultados recientes. 
  
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

**Botón Agregar**

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios agregar y personalizar los botones en el cuadro de diálogo. Los usuarios pueden especificar el texto en los botones y se pueden seleccionar qué elementos de la jerarquía de OneNote por cada botón.  <br/> |
|**Sintaxis** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Parameters** <br/> | _bstrText_ &ndash; Una cadena que especifica el texto para que aparezca en el botón. Para personalizar el botón **Aceptar** de forma predeterminada, pase un valor null como **bstrText**.  <br/><br/>_allowedElements_ &ndash; Un **HierarchyElement** que indica qué elementos de jerarquía de OneNote que no sean de solo lectura que se permite un usuario para seleccionar mediante el botón. Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores de uint al equivalente de los tipos de **HierarchyElement** permitidos como un **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_ &ndash; Un **HierarchyElement** que indica qué elementos de la jerarquía de solo lectura de OneNote que se permite un usuario para seleccionar mediante el botón. Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores de los tipos de **HierarchyElement** permitidos como un **HierarchyElement**equivalentes de **uint** .<br/><br/>  _fDefault_ &ndash; Valor de tipo Boolean que especifica si este botón debe ser el botón predeterminado. Si se establecen varios botones como predeterminada, el último botón especificado se convierte en el botón predeterminado.  <br/> |
   
En el siguiente ejemplo agrega tres botones en el cuadro de diálogo de archivado rápido. El primero de ellos, **todos los**, se puede seleccionar por todos los elementos en el árbol de la jerarquía de OneNote. Los demás, **los blocs de notas** y **las páginas**, pueden seleccionar sólo si sus elementos correspondientes, los blocs de notas y las páginas, se seleccionan.
  
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
|**Descripción** <br/> |Muestra el cuadro de diálogo de archivado rápido desde un subproceso nuevo. Toma una referencia a la interfaz **IQuickFilingDialogCallback** , cuyo **OnDialogClosed** llamará al método una vez que se cierra el cuadro de diálogo.  <br/> |
|**Sintaxis** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Parameters** <br/> | _piCallback_ &ndash; Una referencia a la interfaz de **IQuickFilingDialogCallback** que se creará una instancia una vez que se cierra el cuadro de diálogo.  <br/> |
   
En el ejemplo siguiente se usa el método **Run** para mostrar el cuadro de diálogo de archivado rápido desde un subproceso nuevo. 
  
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
|**Descripción** <br/> |Indica si se debe expandir o contraer el árbol de la jerarquía.  <br/> |
|**Sintaxis** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Parameters** <br/> | _tcs_ - especifica si el árbol está expandido o contraído.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Descripción** <br/> |Filtra la lista de blocs de notas que se muestran por tipo.  <br/> |
|**Sintaxis** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Parameters** <br/> | _nfo_ - especifica el conjunto de los blocs de notas que se deben filtrar fuera de la lista  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra la opción Crear nuevo bloc de notas en el cuadro de diálogo.  <br/> |
|**Sintaxis** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Parameters** <br/> |Ninguno  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Descripción** <br/> |Agrega un usuario como un editor inicial en un bloc de notas en el cuadro de diálogo de archivado rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Parameters** <br/> | _initialEditor_ - la dirección de correo electrónico del usuario que desea agregar como un editor en el Bloc de notas. Cuando se crea el Bloc de notas mediante el cuadro de diálogo fiscal rápida, se comparte automáticamente con todos los editores inicial.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Descripción** <br/> |Quita todos los editores iniciales desde el cuadro de diálogo de archivado rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Parameters** <br/> |Ninguno  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra el hipervínculo del tema de Ayuda de uso compartido en el cuadro de diálogo de archivado rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Parameters** <br/> |Ninguno  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Interfaz IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Esta interfaz permite al usuario tener acceso a las propiedades del cuadro de diálogo cuando se cierra el cuadro de diálogo. Una vez que se cierra el cuadro de diálogo, OneNote 2013 llama al método de **IQuickFilingDialogCallback.OnDialogClose** en esta interfaz. 
  
Una clase que hereda esta interfaz debe estar definido.
  
### <a name="methods"></a>Métodos

En la siguiente sección se describe los métodos asociados con las interfaces detalladas anteriormente.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios agregar la funcionalidad para capturar y utilizar la selección del usuario desde el cuadro de diálogo. Se llama a este método después de cerrar el cuadro de diálogo de archivado rápido. Este método es una función que tienen interfaces de **IQuickFilingDialogCallback** para definir.  <br/> |
|**Sintaxis** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Parameters** <br/> | _cuadro de diálogo_ &ndash; El objeto **IQuickFilingDialog** que llamó al método **OnDialogClose** .  <br/> |
   
El ejemplo siguiente es una interfaz de **IQuickFilingDialogCallback** de ejemplo. El método **OnDialogClose** imprime la selección del usuario desde el cuadro de diálogo fiscal rápido en la consola. 
  
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

En el ejemplo de código siguiente se abre un cuadro de diálogo de archivado rápido que tiene un título personalizado, descripción, lista de resultados recientes, profundidad de árbol, casilla de verificación y los botones. El usuario seleccionado el elemento, que se ha presionado el botón, y el estado de la casilla de verificación se mostrará en una ventana de la consola cuando se cierra el cuadro de diálogo. Para ver el botón de página habilitado, el usuario tendrá que buscar una página y selecciónelo, debido a que se establece la profundidad de árbol hacia abajo a las secciones. El cuadro de diálogo no es un elemento secundario de cualquier ventana.
  
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

## <a name="see-also"></a>Vea también

- [Referencia para desarrolladores de OneNote](onenote-developer-reference.md)


---
title: Interfaces de cuadro de diálogo Archivado rápido (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: En este tema se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo Archivo rápido en OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425340"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>Interfaces de cuadro de diálogo Archivado rápido (OneNote)

En este tema se describen las interfaces que puede usar para personalizar mediante programación el cuadro de diálogo Archivo rápido en OneNote 2013.
  
## <a name="quick-filing-dialog-box"></a>Cuadro de diálogo Archivo rápido

El cuadro de diálogo Archivo rápido de OneNote 2013 es un cuadro de diálogo personalizable que permite a los usuarios seleccionar una ubicación dentro de la OneNote jerarquía. Las ubicaciones seleccionables incluyen blocs de notas, grupos de secciones, secciones, páginas y subpáginas. El cuadro de diálogo se usa tanto en la aplicación OneNote como en aplicaciones externas a través de la API OneNote 2013. La figura 1 muestra el cuadro de diálogo Archivo rápido en su estado predeterminado.
  
**Figura 1. Cuadro de diálogo Archivo rápido sin personalizaciones**

![Cuadro de diálogo Archivo rápido sin personalizaciones]Cuadro de diálogo(media/ON15Con_quick_filing_dialog.jpg "Archivo rápido sin personalizaciones")
  
Dentro del cuadro de diálogo, los usuarios pueden navegar por la jerarquía Todos los blocs de notas para buscar ubicaciones específicas o buscar en la estructura OneNote árbol escribiendo en el cuadro de texto. Los aspectos del cuadro de diálogo que se pueden personalizar incluyen el título, la descripción, la lista de resultados recientes, el texto y el estado de la casilla, la profundidad del árbol, los botones y los tipos de ubicación seleccionables.

Puede acceder a la funcionalidad del cuadro de diálogo Archivo rápido a través de dos OneNote interfaces de 2013. La **interfaz IQuickFilingDialog** permite a los usuarios crear instancias, configurar y ejecutar el cuadro de diálogo. Se llama a la interfaz **IQuickFilingDialogCallback** después de cerrar el cuadro de diálogo. El cuadro de diálogo se ejecuta en el proceso de OneNote, por lo que se necesita un mecanismo para mantener el subproceso del cuadro de diálogo en ejecución y, a continuación, capturar la selección del usuario y el estado del cuadro de diálogo cuando se cierra. 
  
## <a name="iquickfilingdialog-interface"></a>Interfaz IQuickFilingDialog
<a name="odc_IQuickFilingDialog"> </a>

Esta interfaz permite al usuario personalizar y ejecutar el cuadro de diálogo. El usuario puede crear una instancia de un cuadro de diálogo a través **de la clase Application** mediante el método **Application.QuickFilingDialog.** El método devuelve una instancia del cuadro de diálogo. Una vez establecidas las propiedades del cuadro de diálogo, se usa el método **IQuickFilingDialog.Run** para ejecutar el cuadro de diálogo. Este método ejecuta el cuadro de diálogo en un nuevo subproceso. 
  
**Properties**

|**Nombre**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |Obtiene o establece el texto del título que aparece en la barra de título de la ventana del cuadro de diálogo.  <br/> |
|**Descripción** <br/> |string  <br/> |Obtiene o establece la descripción del texto para indicar al usuario qué seleccionar. Este valor puede ser texto de varias líneas.  <br/> |
|**CheckboxText** <br/> |string  <br/> |Obtiene o establece el texto que sigue a la casilla. Si este valor se establece en una cadena no vacía, aparecerá una casilla en el cuadro de diálogo. Si el valor es una cadena vacía, no aparece ninguna casilla.  <br/> |
|**CheckboxState** <br/> |bool  <br/> |Obtiene o establece el estado de la casilla. Si el valor se establece en **false,** la casilla se desactiva cuando se inicia el cuadro de diálogo. Si el valor se establece en **true,** la casilla se activa cuando se inicia el cuadro de diálogo siempre que **CheckboxText** sea una cadena no vacía.  <br/> |
|**WindowHandle** <br/> |ulong  <br/> |Obtiene el identificador de identificador de la ventana del cuadro de diálogo Archivo rápido.  <br/> |
|**TreeDepth** <br/> |**HierarchyElement** <br/> |Obtiene o establece la profundidad del OneNote debe mostrarse en la sección Todos los blocs de notas. De forma predeterminada, el árbol se muestra hasta las secciones. Esta propiedad no afecta al tipo de elementos que se pueden seleccionar.  <br/> Si **TreeDepth** se establece en un elemento inferior en la jerarquía OneNote que puede seleccionar cualquiera de los botones, la profundidad de árbol mostrada será el elemento seleccionable más bajo posible. Es decir, si la profundidad del árbol está configurada para mostrarse en páginas, pero el elemento seleccionable más bajo es una sección, el árbol se muestra en secciones.  <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |Obtiene o establece el identificador de identificador de la ventana primaria del cuadro de diálogo. Si se establece esta propiedad, el cuadro de diálogo Archivo rápido será modal en la ventana principal asignada cuando se abra el cuadro de diálogo. Es decir, un usuario no podrá acceder a la ventana principal hasta que se cierre el cuadro de diálogo Archivo rápido.  <br/> |
|**Position** <br/> |tagPOINT  <br/> |Obtiene o establece la posición de la ventana en relación con la pantalla. De forma predeterminada, el cuadro de diálogo aparece en medio de la ventana principal o del escritorio.  <br/> |
|**SelectedItem** <br/> |string  <br/> |Obtiene el identificador de objeto de la OneNote seleccionada por el usuario cuando se cierra el cuadro de diálogo. Si el usuario hace clic en el **botón Cancelar,** el objeto se establece en null.  <br/> |
|**PressedButton** <br/> |ulong  <br/> |Obtiene qué botón se hizo clic cuando se cerró el cuadro de diálogo. Si se **hizo** clic en el botón Cancelar, esta propiedad devuelve un valor de -1. Todos los demás botones tienen asignados valores enteros de 0, incrementados en 1 para cada botón agregado al cuadro de diálogo. El valor entero del botón **Aceptar** predeterminado es 0.  <br/> |
   
### <a name="methods"></a>Métodos

**SetRecentResults**

|||
|:-----|:-----|
|**Descripción** <br/> |Establece qué lista de resultados recientes se mostrará en el cuadro de diálogo Archivo rápido e indica si se deben incluir algunas ubicaciones de archivado especiales en la lista. Los usuarios pueden seleccionar una lista de resultados reciente de la [enumeración RecentResultType.](enumerations-onenote-developer-reference.md#odc_RecentResultType) Los usuarios también pueden elegir agregar las siguientes opciones a la lista: Sección actual, Página actual o Notas sin archivo. Si **se selecciona RecentResultType.rrtNone,** no se muestra ninguna lista de resultados reciente.  <br/> |
|**Sintaxis** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**Parámetros** <br/> | _recentResults_ &ndash; Un objeto de tipo **RecentResultType** que indica qué lista de resultados recientes, si la hay, debe aparecer. Si **rrtNone** está seleccionado, no aparece ninguna lista de resultados reciente en el cuadro de diálogo.<br/><br/>  _fShowCurrentSection_ &ndash; Valor booleano que indica si la sección actual debe incluirse en la lista de resultados reciente.<br/><br/>  _fShowCurrentPage_ &ndash; Valor booleano que indica si la página actual debe incluirse en la lista de resultados reciente.<br/><br/>  _fShowUnfiledNotes_ &ndash; Valor booleano que indica si la sección Notas sin archivo debe incluirse en la lista de resultados reciente.  <br/> |
   
> [!NOTE]
> Si no se puede seleccionar una ubicación de archivado especial mediante cualquiera de los botones del cuadro de diálogo, no se muestra en la lista. Si no se encuentra ningún elemento seleccionable en la lista de resultados recientes, no se muestra ninguna lista de resultados reciente. 
  
En el ejemplo siguiente se usa el **método SetRecentResults** para mostrar la sección actual, la página actual y la sección Notas sin archivo en la lista de resultados reciente. 
  
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
|**Descripción** <br/> |Permite a los usuarios agregar y personalizar botones en el cuadro de diálogo. Los usuarios pueden especificar el texto de los botones y qué elementos de la jerarquía OneNote pueden seleccionarse mediante cada botón.  <br/> |
|**Sintaxis** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**Parámetros** <br/> | _bstrText_ &ndash; Cadena que especifica el texto que se mostrará en el botón. Para personalizar el botón **aceptar** predeterminado, pase un valor nulo como **bstrText**.  <br/><br/>_allowedElements_ &ndash; HierarchyElement **que** indica qué elementos de jerarquía no de solo OneNote que un usuario puede seleccionar mediante el botón. Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores equivalentes uint de los tipos **HierarchyElement** permitidos como **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_ &ndash; HierarchyElement **que** indica qué elementos OneNote jerarquía de solo lectura que un usuario puede seleccionar mediante el botón. Para seleccionar varios elementos, el usuario debe pasar el operador **OR** para todos los valores **equivalentes uint** de los tipos **HierarchyElement** permitidos como **HierarchyElement**.<br/><br/>  _fDefault_ &ndash; Valor booleano que especifica si este botón debe ser el botón predeterminado. Si varios botones se establecen como predeterminados, el último botón especificado se convierte en el botón predeterminado.  <br/> |
   
En el siguiente ejemplo se agregan tres botones al cuadro de diálogo Archivo rápido. El primero, **All**, puede seleccionarse por todos los elementos del OneNote jerarquía. Los demás, **Blocs de notas** **y** páginas , solo se pueden seleccionar si sus elementos correspondientes, Blocs de notas y páginas, están seleccionados.
  
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
|**Descripción** <br/> |Muestra el cuadro de diálogo Archivo rápido de un nuevo subproceso. Hace referencia a la **interfaz IQuickFilingDialogCallback,** cuyo **método OnDialogClosed** se llamará una vez que se cierre el cuadro de diálogo.  <br/> |
|**Sintaxis** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**Parámetros** <br/> | _piCallback_ &ndash; Una referencia a la **interfaz IQuickFilingDialogCallback** que se instanciará una vez que se cierre el cuadro de diálogo.  <br/> |
   
En el ejemplo siguiente se usa **el método Run** para mostrar el cuadro de diálogo Archivo rápido desde un nuevo subproceso. 
  
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
|**Descripción** <br/> |Indica si el árbol de jerarquía debe expandirse o contraerse.  <br/> |
|**Sintaxis** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**Parámetros** <br/> | _tcs:_ especifica si el árbol está expandido o contraído.  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**Descripción** <br/> |Filtra la lista de blocs de notas que se muestra por tipo.  <br/> |
|**Sintaxis** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**Parámetros** <br/> | _nfo:_ especifica el conjunto de blocs de notas que se van a filtrar fuera de la lista  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra la opción crear nuevo bloc de notas en el cuadro de diálogo.  <br/> |
|**Sintaxis** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**Parámetros** <br/> |Ninguno  <br/> |
   
**AddInitialEditor**

|||
|:-----|:-----|
|**Descripción** <br/> |Agrega un usuario como editor inicial a un bloc de notas en el cuadro de diálogo Archivo rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**Parámetros** <br/> | _initialEditor:_ la dirección de correo electrónico del usuario que desea agregar como editor al bloc de notas. Cuando el bloc de notas se crea mediante el cuadro de diálogo Archivo rápido, se comparte automáticamente con todos los editores iniciales.  <br/> |
   
**ClearInitialEditors**

|||
|:-----|:-----|
|**Descripción** <br/> |Quita todos los editores iniciales del cuadro de diálogo Archivo rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**Parámetros** <br/> |Ninguno  <br/> |
   
**ShowSharingHyperlink**

|||
|:-----|:-----|
|**Descripción** <br/> |Muestra el hipervínculo Tema de ayuda para uso compartido en el cuadro de diálogo Archivo rápido.  <br/> |
|**Sintaxis** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**Parámetros** <br/> |Ninguno  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>Interfaz IQuickFilingDialogCallback
<a name="odc_IQuickFilingDialog"> </a>

Esta interfaz permite al usuario tener acceso a las propiedades del cuadro de diálogo después de cerrar el cuadro de diálogo. Una vez que se cierra el cuadro de diálogo, OneNote 2013 llama al método **IQuickFilingDialogCallback.OnDialogClose** en esta interfaz. 
  
Debe definirse una clase que herede esta interfaz.
  
### <a name="methods"></a>Métodos

En la siguiente sección se describen los métodos asociados con las interfaces detalladas anteriormente.
  
**OnDialogClosed**

|||
|:-----|:-----|
|**Descripción** <br/> |Permite a los usuarios agregar funcionalidad para capturar y usar la selección de usuario desde el cuadro de diálogo. Se llama a este método después de cerrar el cuadro de diálogo Archivo rápido. Este método es una función que las interfaces **IQuickFilingDialogCallback** tienen que definir.  <br/> |
|**Sintaxis** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**Parámetros** <br/> | _cuadro de diálogo_ &ndash; El **objeto IQuickFilingDialog** que llamó al **método OnDialogClose.**  <br/> |
   
El ejemplo siguiente es una interfaz **IQuickFilingDialogCallback de** ejemplo. El **método OnDialogClose** imprime la selección del usuario desde el cuadro de diálogo Archivo rápido en la consola. 
  
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

En el siguiente ejemplo de código se abre un cuadro de diálogo Archivo rápido que tiene un título personalizado, una descripción, una lista de resultados recientes, una profundidad de árbol, una casilla de verificación y botones. El elemento seleccionado, el botón presionado y el estado de la casilla del usuario se mostrarán en una ventana de consola cuando se cierre el cuadro de diálogo. Para ver el botón de página habilitado, el usuario tendrá que buscar una página y seleccionarla, ya que la profundidad del árbol se establece en secciones. El cuadro de diálogo no es un elemento secundario de ninguna ventana.
  
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


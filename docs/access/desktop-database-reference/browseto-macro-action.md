---
title: Explorar (acción de macro)
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15009ca039d5df06bc732f4b58c066ad8f8d67c9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603766"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="86ae7-102">Explorar (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="86ae7-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="86ae7-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="86ae7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="86ae7-p101">Puede utilizar la acción **Explorar** para desplazarse entre objetos en su lugar. También puede cambiar el objeto de origen de un control de subformulario especificando el argumento Ruta de acceso al control de subformulario. Utilice la acción **Explorar** para desplazarse de formulario1 a formulario2 sin abrir una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="86ae7-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="86ae7-107">Valores</span><span class="sxs-lookup"><span data-stu-id="86ae7-107">Setting</span></span>

<span data-ttu-id="86ae7-108">La acción **Explorar** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="86ae7-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86ae7-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="86ae7-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="86ae7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="86ae7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86ae7-111">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="86ae7-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="86ae7-112">El tipo de objeto en el que se va a examinar.</span><span class="sxs-lookup"><span data-stu-id="86ae7-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86ae7-113">Nombre de objeto</span><span class="sxs-lookup"><span data-stu-id="86ae7-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="86ae7-114">El objeto que se carga dentro del control de subformulario al que hace referencia al argumento Ruta de acceso al control de subformulario.</span><span class="sxs-lookup"><span data-stu-id="86ae7-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86ae7-115">Ruta de acceso al control de subformulario</span><span class="sxs-lookup"><span data-stu-id="86ae7-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="86ae7-116">Si se especifica, la ruta de acceso desde el formulario principal de la aplicación para el subformulario de destino control que carga el objeto especificado por el argumento nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="86ae7-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86ae7-117">Condición WHERE</span><span class="sxs-lookup"><span data-stu-id="86ae7-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="86ae7-118">Si se especifica, reemplaza la condición WHERE del origen de registros del objeto.</span><span class="sxs-lookup"><span data-stu-id="86ae7-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86ae7-119">Page</span><span class="sxs-lookup"><span data-stu-id="86ae7-119">Page</span></span></p></td>
<span data-ttu-id="86ae7-120"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="86ae7-120"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="86ae7-p102">Si especifica, se establece la página del formulario continuo que se realizarán la página actual. Este argumento sólo es web.</span><span class="sxs-lookup"><span data-stu-id="86ae7-p102">If specified, sets the page of the continuous form that will be made the current page. This argument is Web only.</span></span></p></td>
=======
<td><p><span data-ttu-id="86ae7-123">Si especifica, se establece la página del formulario continuo que se realizarán la página actual.</span><span class="sxs-lookup"><span data-stu-id="86ae7-123">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="86ae7-124">Este argumento es sólo web.</span><span class="sxs-lookup"><span data-stu-id="86ae7-124">This argument is web only.</span></span></p></td><span data-ttu-id="86ae7-125">
>>>>>>>patrón</span><span class="sxs-lookup"><span data-stu-id="86ae7-125">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86ae7-126">Modo de datos</span><span class="sxs-lookup"><span data-stu-id="86ae7-126">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="86ae7-127">Si se especifica, es el modo de entrada de datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="86ae7-127">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="86ae7-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86ae7-128">Remarks</span></span>

<span data-ttu-id="86ae7-129">El argumento Ruta de acceso al control de subformulario debe especificarse mediante la sintaxis en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="86ae7-129">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="86ae7-p104">En este ejemplo, el formulario principal es el formulario de nivel superior en la aplicación de cliente de Access. El argumento Ruta de acceso al control de subformulario debe especificar alternativamente los nombres de control de formulario y subformulario que van del formulario principal al control de subformulario que es el contenedor del objeto especificado por el argumento Nombre de objeto. Cada control del subformulario especificado debe ser un control en el formulario que lo precede. La ruta de acceso debe terminar con un control de subformulario.</span><span class="sxs-lookup"><span data-stu-id="86ae7-p104">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="86ae7-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86ae7-134">Example</span></span>

<span data-ttu-id="86ae7-135">En el ejemplo siguiente se muestra cómo usar la acción explorar para abrir un informe en un control de subformulario o dentro de un control de navegación.</span><span class="sxs-lookup"><span data-stu-id="86ae7-135">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="86ae7-136">**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="86ae7-136">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```




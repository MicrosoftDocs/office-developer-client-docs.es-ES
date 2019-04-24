---
title: Explorar (acción de macro)
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296776"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="e3ee3-102">Explorar (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="e3ee3-102">BrowseTo macro action</span></span>

<span data-ttu-id="e3ee3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3ee3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3ee3-p101">Puede utilizar la acción **Explorar** para desplazarse entre objetos en su lugar. También puede cambiar el objeto de origen de un control de subformulario especificando el argumento Ruta de acceso al control de subformulario. Utilice la acción **Explorar** para desplazarse de formulario1 a formulario2 sin abrir una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="e3ee3-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="e3ee3-107">Setting</span></span>

<span data-ttu-id="e3ee3-108">La acción **Explorar** tiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e3ee3-109">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="e3ee3-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e3ee3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3ee3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e3ee3-111">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="e3ee3-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="e3ee3-112">El tipo de objeto en el que se va a explorar.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ee3-113">Nombre de objeto</span><span class="sxs-lookup"><span data-stu-id="e3ee3-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="e3ee3-114">El objeto que se carga dentro del control de subformulario al que hace referencia al argumento Ruta de acceso al control de subformulario.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ee3-115">Ruta de acceso al control de subformulario</span><span class="sxs-lookup"><span data-stu-id="e3ee3-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="e3ee3-116">Si se especifica, la ruta de acceso del formulario principal de la aplicación al control de subformulario de destino que carga el objeto especificado por el argumento nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ee3-117">Condición WHERE</span><span class="sxs-lookup"><span data-stu-id="e3ee3-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="e3ee3-118">Si se especifica, reemplaza la condición WHERE del origen de registro de objeto.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e3ee3-119">Page</span><span class="sxs-lookup"><span data-stu-id="e3ee3-119">Page</span></span></p></td>
<td><p><span data-ttu-id="e3ee3-120">Si especifica, se establece la página del formulario continuo que se realizarán la página actual.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="e3ee3-121">Este argumento es solo Web.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e3ee3-122">Modo de datos</span><span class="sxs-lookup"><span data-stu-id="e3ee3-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="e3ee3-123">Si se especifica, es el modo de entrada de datos del formulario.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e3ee3-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3ee3-124">Remarks</span></span>

<span data-ttu-id="e3ee3-125">El argumento Ruta de acceso al control de subformulario debe especificarse mediante la sintaxis en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="e3ee3-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="e3ee3-p103">En este ejemplo, el formulario principal es el formulario de nivel superior en la aplicación de cliente de Access. El argumento Ruta de acceso al control de subformulario debe especificar alternativamente los nombres de control de formulario y subformulario que van del formulario principal al control de subformulario que es el contenedor del objeto especificado por el argumento Nombre de objeto. Cada control del subformulario especificado debe ser un control en el formulario que lo precede. La ruta de acceso debe terminar con un control de subformulario.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-p103">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="e3ee3-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3ee3-130">Example</span></span>

<span data-ttu-id="e3ee3-131">En el siguiente ejemplo, se muestra cómo usar la acción browseTo para abrir un informe en un control de subformulario o dentro de un control de navegación.</span><span class="sxs-lookup"><span data-stu-id="e3ee3-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="e3ee3-132">**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e3ee3-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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




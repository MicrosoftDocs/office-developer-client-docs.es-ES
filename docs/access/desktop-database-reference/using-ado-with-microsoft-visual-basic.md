---
title: Utilizar ADO con Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e209c00742772d8d3294be4a74772526c3c29c2
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861025"
---
# <a name="using-ado-with-microsoft-visual-basic"></a><span data-ttu-id="5b6df-102">Uso de ADO con Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b6df-102">Using ADO with Microsoft Visual Basic</span></span>


<span data-ttu-id="5b6df-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b6df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5b6df-p101">Configurar un proyecto de ADO y escribir código de ADO es un procedimiento similar en Visual Basic y Visual Basic para Aplicaciones. En este tema se aborda el uso de ADO con Visual Basic y Visual Basic para Aplicaciones, así como las diferencias.</span><span class="sxs-lookup"><span data-stu-id="5b6df-p101">Setting up an ADO project and writing ADO code is similar whether you use Visual Basic or Visual Basic for Applications. This topic addresses using ADO with both Visual Basic and Visual Basic for Applications and notes any differences.</span></span>

## <a name="referencing-the-ado-library"></a><span data-ttu-id="5b6df-106">Hacer referencia a la biblioteca de ADO</span><span class="sxs-lookup"><span data-stu-id="5b6df-106">Referencing the ADO Library</span></span>

<span data-ttu-id="5b6df-107">El proyecto debe hacer referencia a la biblioteca de ADO.</span><span class="sxs-lookup"><span data-stu-id="5b6df-107">The ADO library must be referenced by your project.</span></span>

<span data-ttu-id="5b6df-108">**Para hacer referencia a ADO desde Microsoft Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="5b6df-108">**To reference ADO from Microsoft Visual Basic**</span></span>

1.  <span data-ttu-id="5b6df-109">En Visual Basic, en el menú **Proyecto**, seleccione **Referencias**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-109">In Visual Basic, from the **Project** menu, select **References...**.</span></span>

2.  <span data-ttu-id="5b6df-p102">Seleccione **Biblioteca de Microsoft ActiveX Data Objects x.x** en la lista. Compruebe que estén seleccionadas al menos las siguientes bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="5b6df-p102">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="5b6df-112">Visual Basic para Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5b6df-112">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="5b6df-113">Objetos y procedimientos del motor en tiempo de ejecución de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b6df-113">Visual Basic runtime objects and procedures</span></span>
    
    - <span data-ttu-id="5b6df-114">Objetos y procedimientos de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b6df-114">Visual Basic objects and procedures</span></span>
    
    - <span data-ttu-id="5b6df-115">Automatización OLE</span><span class="sxs-lookup"><span data-stu-id="5b6df-115">OLE Automation</span></span>

3.  <span data-ttu-id="5b6df-116">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-116">Click **OK**.</span></span>

<span data-ttu-id="5b6df-117">ADO se puede utilizar con la misma facilidad con Visual Basic para Aplicaciones mediante, por ejemplo, Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5b6df-117">You can use ADO just as easily with Visual Basic for Applications, using Microsoft Access, for example.</span></span>

<span data-ttu-id="5b6df-118">**Para hacer referencia a ADO desde Microsoft Access**</span><span class="sxs-lookup"><span data-stu-id="5b6df-118">**To reference ADO from Microsoft Access**</span></span>

1.  <span data-ttu-id="5b6df-119">En Microsoft Access, seleccione o cree un módulo en la pestaña **Módulos** de la ventana **Base de datos**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-119">In Microsoft Access, select or create a module from the **Modules** tab in the **Database** window.</span></span>

2.  <span data-ttu-id="5b6df-120">En el menú **Herramientas**, seleccione **Referencias**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-120">From the **Tools** menu, select **References...**.</span></span>

3.  <span data-ttu-id="5b6df-p103">Seleccione **Biblioteca de Microsoft ActiveX Data Objects x.x** en la lista. Compruebe que estén seleccionadas al menos las siguientes bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="5b6df-p103">Select **Microsoft ActiveX Data Objects x.x Library** from the list. Verify that at least the following libraries are also selected:</span></span>
    
    - <span data-ttu-id="5b6df-123">Visual Basic para Aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5b6df-123">Visual Basic for Applications</span></span>
    
    - <span data-ttu-id="5b6df-124">Biblioteca de objetos de Microsoft Access 11.0 (o posterior)</span><span class="sxs-lookup"><span data-stu-id="5b6df-124">Microsoft Access 11.0 Object Library (or later)</span></span>

4.  <span data-ttu-id="5b6df-125">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-125">Click **OK**.</span></span>

## <a name="creating-ado-objects-in-visual-basic"></a><span data-ttu-id="5b6df-126">Crear objetos ADO en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b6df-126">Creating ADO Objects in Visual Basic</span></span>

<span data-ttu-id="5b6df-127">Para crear una variable de automatización y una instancia de un objeto para esa variable, se pueden utilizar dos métodos: **Dim** o **CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-127">To create an automation variable and an instance of an object for that variable, you can use two methods: **Dim** or **CreateObject**.</span></span>

## <a name="dim"></a><span data-ttu-id="5b6df-128">Dim</span><span class="sxs-lookup"><span data-stu-id="5b6df-128">Dim</span></span>

<span data-ttu-id="5b6df-129">Se puede utilizar la palabra clave **New** con **Dim** para declarar y crear instancias de los objetos ADO en un solo paso:</span><span class="sxs-lookup"><span data-stu-id="5b6df-129">You can use the **New** keyword with **Dim** to declare and instantiate ADO objects in one step:</span></span>

```vb 
 
Dim conn As New ADODB.Connection 
```

<span data-ttu-id="5b6df-130">Asimismo, la declaración de la instrucción **Dim** y la creación de instancias de objetos pueden constar de dos pasos:</span><span class="sxs-lookup"><span data-stu-id="5b6df-130">Alternately, the **Dim** statement declaration and object instantiation can also be two steps:</span></span>

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```


> [!NOTE]
> <P><span data-ttu-id="5b6df-p104">No es necesario utilizar explícitamente el identificador de programa ADODB con la instrucción <STRONG>Dim</STRONG>, suponiendo que se ha hecho correctamente referencia a la biblioteca de ADO en el proyecto. Sin embargo, su uso garantiza que no habrá conflictos de nomenclatura con otras bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="5b6df-p104">It is not required to explicitly use the ADODB progid with the <STRONG>Dim</STRONG> statement, assuming you have properly referenced the ADO library in your project. However, using it ensures that you won't have naming conflicts with other libraries.</span></span></P>



<span data-ttu-id="5b6df-133">Por ejemplo, si se incluyen referencias a ADO y DAO en el mismo proyecto, se deberá incluir un calificador para especificar el modelo de objetos que se va a usar cuando se creen instancias de los objetos **Recordset**, como en el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="5b6df-133">For example, if you include references to both ADO and DAO in the same project, you should include a qualifier to specify which object model to use when instantiating **Recordset** objects, as in the following code:</span></span>  
<span data-ttu-id="5b6df-134">Dim adoRS As ADODB. Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5b6df-134">Dim adoRS As ADODB.Recordset</span></span>  
  
<span data-ttu-id="5b6df-135">Dim daoRS As DAO. Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="5b6df-135">Dim daoRS As DAO.Recordset</span></span>

## <a name="createobject"></a><span data-ttu-id="5b6df-136">CreateObject</span><span class="sxs-lookup"><span data-stu-id="5b6df-136">CreateObject</span></span>

<span data-ttu-id="5b6df-137">Con el método **CreateObject**, la declaración y la creación de instancias de objetos deben constar de dos pasos diferenciados:</span><span class="sxs-lookup"><span data-stu-id="5b6df-137">With the **CreateObject** method, the declaration and object instantiation must be two discrete steps:</span></span>

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

<span data-ttu-id="5b6df-p105">Los objetos cuyas instancias se crean con **CreateObject** se enlazan en tiempo de ejecución, lo que significa que no tienen establecimiento inflexible de tipos y que la opción para completar la línea de comandos no está habilitada. Sin embargo, permite omitir la referencia a la biblioteca de ADO desde el proyecto y permite crear instancias de versiones específicas de los objetos. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="5b6df-p105">Objects instantiated with **CreateObject** are late-bound, which means that they are not strongly typed and command-line completion is disabled. However, it does allow you to skip referencing the ADO library from your project, and enables you to instantiate specific versions of objects. For example:</span></span>

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

<span data-ttu-id="5b6df-141">Para ello, también se puede crear específicamente una referencia a la versión 2.0 de la Biblioteca de tipos de ADO y crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="5b6df-141">You could also accomplish this by specifically creating a reference to the ADO version 2.0 type library and creating the object.</span></span>

<span data-ttu-id="5b6df-142">La creación de instancias de los objetos con el método **CreateObject** suele ser más lenta que cuando se utiliza la instrucción **Dim**.</span><span class="sxs-lookup"><span data-stu-id="5b6df-142">Instantiating objects with the **CreateObject** method is typically slower than using the **Dim** statement.</span></span>

## <a name="handling-events"></a><span data-ttu-id="5b6df-143">Controlar eventos</span><span class="sxs-lookup"><span data-stu-id="5b6df-143">Handling Events</span></span>

<span data-ttu-id="5b6df-p106">Para controlar los eventos de ADO en Microsoft Visual Basic, es preciso declarar una variable en el nivel de módulo mediante la palabra clave **WithEvents**. La variable se puede declarar únicamente como parte de un módulo de clase y debe declararse en el nivel de módulo. Para obtener una descripción más completa de cómo controlar los eventos de ADO, vea [Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md).</span><span class="sxs-lookup"><span data-stu-id="5b6df-p106">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword. The variable can be declared only as part of a class module and must be declared at the module level. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

## <a name="visual-basic-examples"></a><span data-ttu-id="5b6df-147">Ejemplos de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b6df-147">Visual Basic Examples</span></span>

<span data-ttu-id="5b6df-148">La documentación de ADO incluye numerosos ejemplos de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b6df-148">Many Visual Basic examples are included with the ADO documentation.</span></span> <span data-ttu-id="5b6df-149">Para obtener más información, vea [ejemplos de código de ADO en Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="5b6df-149">For more information, see [ADO code examples in Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).</span></span>


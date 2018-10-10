---
title: AbrirMóduloVisualBasic (acción de macro)
TOCTitle: OpenVisualBasicModule Macro Action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9c57bb28de25ebc540c4e4eb3804a714969e2ac6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486366"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="86eb9-102">AbrirMóduloVisualBasic (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="86eb9-102">OpenVisualBasicModule Macro Action</span></span>


<span data-ttu-id="86eb9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="86eb9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="86eb9-p101">Puede usar la acción **AbrirMóduloVisualBasic** para abrir un módulo especificado de Visual Basic para Aplicaciones (VBA) en un procedimiento especificado. Puede tratarse de un procedimiento Sub, un procedimiento de función o un procedimiento de evento.</span><span class="sxs-lookup"><span data-stu-id="86eb9-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>


> [!NOTE]
> <P><span data-ttu-id="86eb9-p102">[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</span><span class="sxs-lookup"><span data-stu-id="86eb9-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="86eb9-108">Configuración</span><span class="sxs-lookup"><span data-stu-id="86eb9-108">Setting</span></span>

<span data-ttu-id="86eb9-109">La acción **AbrirMóduloVisualBasic** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="86eb9-109">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86eb9-110">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="86eb9-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="86eb9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="86eb9-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86eb9-112"><strong>Nombre del módulo</strong></span><span class="sxs-lookup"><span data-stu-id="86eb9-112"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="86eb9-113">El nombre del módulo que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="86eb9-113">The name of the module you want to open.</span></span> <span data-ttu-id="86eb9-114">Deje este argumento en blanco si desea buscar todos los módulos estándar de la base de datos para un procedimiento y abrir el módulo correspondiente a ese procedimiento.</span><span class="sxs-lookup"><span data-stu-id="86eb9-114">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="86eb9-115">Si ejecuta una macro que contiene la acción <strong>AbrirMóduloVisualBasic</strong> en una base de datos de biblioteca, Microsoft Access primero buscar el módulo con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="86eb9-115">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86eb9-116"><strong>Nombre del procedimiento</strong></span><span class="sxs-lookup"><span data-stu-id="86eb9-116"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="86eb9-p104">Nombre del procedimiento en el que se desea abrir el módulo. Si deja en blanco este argumento, el módulo se abre en la sección Declaraciones.</span><span class="sxs-lookup"><span data-stu-id="86eb9-p104">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="86eb9-119">[!NOTA] Debe escribir un nombre válido en el argumento <STRONG>Nombre del módulo</STRONG> o <STRONG>Nombre del procedimiento</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="86eb9-119">You must enter a valid name in either the <STRONG>Module Name</STRONG> or <STRONG>Procedure Name</STRONG> argument.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="86eb9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86eb9-120">Remarks</span></span>

<span data-ttu-id="86eb9-121">Puede usar esta acción para abrir un procedimiento de evento especificando el argumento **Nombre del módulo** y el argumento **Nombre del procedimiento** .</span><span class="sxs-lookup"><span data-stu-id="86eb9-121">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="86eb9-122">Por ejemplo, para abrir el procedimiento de evento **Click** del botón ImprimirFactura del formulario Pedidos, establezca el argumento **Nombre del módulo** en **formulario.pedidos** y establezca el argumento **Nombre del procedimiento** en **ImprimirFactura\_haga clic en**.</span><span class="sxs-lookup"><span data-stu-id="86eb9-122">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="86eb9-123">Para ver un procedimiento de evento de un formulario o informe, éste debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="86eb9-123">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="86eb9-124">De forma similar, para abrir un procedimiento en un módulo de clase, debe especificar el nombre del módulo, si bien el módulo de clase no tiene que estar abierto.</span><span class="sxs-lookup"><span data-stu-id="86eb9-124">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="86eb9-125">Para abrir un procedimiento privado, el módulo que lo contiene debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="86eb9-125">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="86eb9-p106">Esta acción tiene el mismo efecto que hacer clic con el botón secundario en un módulo en el panel de navegación y, a continuación, hacer clic en **Vista Diseño**. Esta acción también permite especificar un nombre de procedimiento y buscar procedimientos en los módulos estándar de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="86eb9-p106">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>


> [!TIP]
> <P><span data-ttu-id="86eb9-p107">[!SUGERENCIA] Puede seleccionar un módulo en el panel de navegación y arrastrarlo hasta una fila de acción de una macro. De esta forma, se crea automáticamente una acción <STRONG>AbrirMóduloVisualBasic</STRONG> que abre el módulo en la sección Declaraciones.</span><span class="sxs-lookup"><span data-stu-id="86eb9-p107">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an <STRONG>OpenVisualBasicModule</STRONG> action that opens the module to the Declarations section.</span></span></P>



<span data-ttu-id="86eb9-130">Para ejecutar la acción **AbrirMóduloVisualBasic** en un módulo de VBA, use el método **OpenModule** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="86eb9-130">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>


---
title: AbrirMóduloVisualBasic (acción de macro)
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288283"
---
# <a name="openvisualbasicmodule-macro-action"></a><span data-ttu-id="cedec-102">AbrirMóduloVisualBasic (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="cedec-102">OpenVisualBasicModule macro action</span></span>

<span data-ttu-id="cedec-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cedec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cedec-p101">Puede usar la acción **AbrirMóduloVisualBasic** para abrir un módulo especificado de Visual Basic para Aplicaciones (VBA) en un procedimiento especificado. Puede tratarse de un procedimiento Sub, un procedimiento de función o un procedimiento de evento.</span><span class="sxs-lookup"><span data-stu-id="cedec-p101">You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="cedec-106">Esta acción no se permitirá si la base de datos no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="cedec-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="cedec-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="cedec-107">Setting</span></span>

<span data-ttu-id="cedec-108">La acción **AbrirMóduloVisualBasic** tiene los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="cedec-108">The **OpenVisualBasicModule** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cedec-109">Argumento de acción</span><span class="sxs-lookup"><span data-stu-id="cedec-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cedec-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cedec-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cedec-111"><strong>Nombre del módulo</strong></span><span class="sxs-lookup"><span data-stu-id="cedec-111"><strong>Module Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cedec-112">Nombre del módulo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="cedec-112">The name of the module you want to open.</span></span> <span data-ttu-id="cedec-113">Deje este argumento en blanco si lo que desea es buscar un procedimiento en todos los módulos estándar de la base de datos y abrir el módulo que lo contenga en ese procedimiento.</span><span class="sxs-lookup"><span data-stu-id="cedec-113">You can leave this argument blank if you want to search all the standard modules in the database for a procedure and open the appropriate module at that procedure.</span></span> <span data-ttu-id="cedec-114">Si ejecuta una macro que contiene la acción <strong>AbrirMóduloVisualBasic</strong> en una base de datos de biblioteca, Microsoft Access primero buscar el módulo con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</span><span class="sxs-lookup"><span data-stu-id="cedec-114">If you run a macro containing the <strong>OpenVisualBasicModule</strong> action in a library database, Microsoft Access first looks for the module with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cedec-115"><strong>Nombre del procedimiento</strong></span><span class="sxs-lookup"><span data-stu-id="cedec-115"><strong>Procedure Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cedec-p103">Nombre del procedimiento en el que se desea abrir el módulo. Si deja en blanco este argumento, el módulo se abre en la sección Declaraciones.</span><span class="sxs-lookup"><span data-stu-id="cedec-p103">The name of the procedure you want to open the module to. If you leave this argument blank, the module opens to the Declarations section.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="cedec-118">Debe escribir un nombre válido en el argumento **Nombre del módulo** o **Nombre del procedimiento**.</span><span class="sxs-lookup"><span data-stu-id="cedec-118">You must enter a valid name in either the **Module Name** or **Procedure Name** argument.</span></span>


## <a name="remarks"></a><span data-ttu-id="cedec-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cedec-119">Remarks</span></span>

<span data-ttu-id="cedec-120">Puede usar esta acción para abrir un procedimiento de evento especificando el argumento **Nombre** de módulo y el argumento **Nombre de** procedimiento.</span><span class="sxs-lookup"><span data-stu-id="cedec-120">You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument.</span></span> <span data-ttu-id="cedec-121">Por ejemplo, para abrir el procedimiento de evento **Click** del botón PrintInvoice en el formulario Orders, establezca el argumento **Module Name** en **Form.Orders** y establezca el argumento Procedure **Name** en **PrintInvoice \_ Click**.</span><span class="sxs-lookup"><span data-stu-id="cedec-121">For example, to open the **Click** event procedure of the PrintInvoice button on the form Orders, set the **Module Name** argument to **Form.Orders** and set the **Procedure Name** argument to **PrintInvoice\_Click**.</span></span> <span data-ttu-id="cedec-122">Para ver un procedimiento de evento de un formulario o informe, éste debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="cedec-122">To view the event procedure for a form or report, the form or report must be open.</span></span>

<span data-ttu-id="cedec-123">De forma similar, para abrir un procedimiento en un módulo de clase, debe especificar el nombre del módulo, si bien el módulo de clase no tiene que estar abierto.</span><span class="sxs-lookup"><span data-stu-id="cedec-123">Similarly, to open a procedure in a class module, you must specify the module name, although the class module does not have to open.</span></span>

<span data-ttu-id="cedec-124">Para abrir un procedimiento privado, el módulo que lo contiene debe estar abierto.</span><span class="sxs-lookup"><span data-stu-id="cedec-124">To open a private procedure, the module containing it must be open.</span></span>

<span data-ttu-id="cedec-p105">Esta acción tiene el mismo efecto que hacer clic con el botón secundario en un módulo en el panel de navegación y, a continuación, hacer clic en **Vista Diseño**. Esta acción también permite especificar un nombre de procedimiento y buscar procedimientos en los módulos estándar de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="cedec-p105">This action has the same effect as right-clicking a module in the Navigation Pane and then clicking **Design View**. This action also enables you to specify a procedure name and to search the standard modules in a database for procedures.</span></span>

> [!TIP]
> <span data-ttu-id="cedec-p106">[!SUGERENCIA] Puede seleccionar un módulo en el panel de navegación y arrastrarlo hasta una fila de acción de una macro. De esta forma, se crea automáticamente una acción **AbrirMóduloVisualBasic** que abre el módulo en la sección Declaraciones.</span><span class="sxs-lookup"><span data-stu-id="cedec-p106">You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.</span></span>

<span data-ttu-id="cedec-129">Para ejecutar la acción **AbrirMóduloVisualBasic** en un módulo de VBA, use el método **OpenModule** del objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="cedec-129">To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.</span></span>


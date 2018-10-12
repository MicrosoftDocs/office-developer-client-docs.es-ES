---
title: EjecutarComandoDeMenú (acción de macro)
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485226"
---
# <a name="runmenucommand-macro-action"></a><span data-ttu-id="c825a-102">EjecutarComandoDeMenú (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="c825a-102">RunMenuCommand Macro Action</span></span>


<span data-ttu-id="c825a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c825a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c825a-104">La acción **EjecutarComandoDeMenú** sirve para ejecutar un comando integrado de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c825a-104">You can use the **RunMenuCommand** action to run a built-in Microsoft Access command.</span></span>

## <a name="setting"></a><span data-ttu-id="c825a-105">Configuración</span><span class="sxs-lookup"><span data-stu-id="c825a-105">Setting</span></span>

<span data-ttu-id="c825a-106">La acción **EjecutarComandoDeMenú** usa el siguiente argumento de acción.</span><span class="sxs-lookup"><span data-stu-id="c825a-106">The **RunMenuCommand** action has the following action argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c825a-107">Argumento de la acción</span><span class="sxs-lookup"><span data-stu-id="c825a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c825a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="c825a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c825a-109"><strong>Command</strong></span><span class="sxs-lookup"><span data-stu-id="c825a-109"><strong>Command</strong></span></span></p></td>
<td><p><span data-ttu-id="c825a-p101">El nombre del comando que desee ejecutar. El cuadro <strong>Comando</strong> muestra los comandos integrados disponibles en Access, por orden alfabético. Este argumento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c825a-p101">The name of the command you want to run. The <strong>Command</strong> box shows the available built-in commands in Access, in alphabetical order. This is a required argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c825a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c825a-113">Remarks</span></span>

<span data-ttu-id="c825a-114">Puede usar la acción **EjecutarComandoDeMenú** para ejecutar un comando de Access desde una barra de menús personalizada, una barra de menús global, un menú contextual personalizado o un menú contextual global.</span><span class="sxs-lookup"><span data-stu-id="c825a-114">You can use the **RunMenuCommand** action to run an Access command from a custom menu bar, global menu bar, custom shortcut menu, or global shortcut menu.</span></span>

<span data-ttu-id="c825a-115">La acción **EjecutarComandoDeMenú** se puede utilizar en una macro con expresiones condicionales para ejecutar un comando según ciertas condiciones.</span><span class="sxs-lookup"><span data-stu-id="c825a-115">You can use the **RunMenuCommand** action in a macro with conditional expressions to run a command depending on certain conditions.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c825a-p102">[!NOTA] Al hacer clic en la pestaña <STRONG>Archivo</STRONG> y <STRONG>Reciente</STRONG>, se muestran las bases de datos utilizadas más recientemente. Puede hacer clic en una de estas bases de datos en lugar de hacer clic en <STRONG>Abrir</STRONG>. Estos elementos de base de datos no aparecen en el cuadro de lista desplegable para el argumento <STRONG>Comando</STRONG>, y no están disponibles cuando se utiliza la acción <STRONG>EjecutarComandoDeMenú</STRONG> en una macro.</span><span class="sxs-lookup"><span data-stu-id="c825a-p102">Clicking the <STRONG>File</STRONG> tab and then clicking <STRONG>Recent</STRONG> shows the most recently used databases. You can click one of these databases instead of clicking <STRONG>Open</STRONG>. These database items don't appear in the drop-down list box for the <STRONG>Command</STRONG> argument, and aren't available by using the <STRONG>RunMenuCommand</STRONG> action in a macro.</span></span></P>



<span data-ttu-id="c825a-p103">Cuando se convierte una base de datos de Access desde una versión anterior, es posible que algunos comandos dejen de estar disponibles. Puede que algún comando haya cambiado de nombre, se haya trasladado a un menú distinto o ya no esté disponible en Access. Las acciones **EjecutarComandoDeMenú** para tales comandos no pueden ser convertidas a acciones **EjecutarComandoDeMenú**. Cuando se abre la macro, Access muestra una acción **EjecutarComandoDeMenú** con un argumento **Comando** en blanco para esos comandos. Deberá modificar la macro y especificar un argumento de comando válido, o eliminar la acción **EjecutarComandoDeMenú**.</span><span class="sxs-lookup"><span data-stu-id="c825a-p103">When you convert an Access database from a previous version of Access, some commands may no longer be available. A command may have been renamed, moved to a different menu, or may no longer be available in Access. The **DoMenuItem** actions for such commands can't be converted to **RunMenuCommand** actions. When you open the macro, Access will display a **RunMenuCommand** action with a blank **Command** argument for such commands. You must edit the macro and enter a valid command argument, or delete the **RunMenuCommand** action.</span></span>

<span data-ttu-id="c825a-p104">Para ejecutar la acción **EjecutarComandoDeMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **RunCommand** del objeto **Application** (equivalente al método **RunCommand** del objeto **DoCmd** ).</span><span class="sxs-lookup"><span data-stu-id="c825a-p104">To run the **RunMenuCommand** action in a Visual Basic for Applications (VBA) module, use the **RunCommand** method of the **Application** object. (This is equivalent to the **RunCommand** method of the **DoCmd** object.)</span></span>

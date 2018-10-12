---
title: RegistrarEvento (acción de macro)
TOCTitle: LogEvent Macro Action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f626dd61782baed2e46aa931891a172fc53c1bde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485412"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="af563-102">RegistrarEvento (acción de macro)</span><span class="sxs-lookup"><span data-stu-id="af563-102">LogEvent Macro Action</span></span>


<span data-ttu-id="af563-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="af563-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="af563-104">La acción **RegistrarEvento** escribe información en la tabla de sistema **USysApplicationLog**.</span><span class="sxs-lookup"><span data-stu-id="af563-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="af563-105">[!NOTA] La acción <STRONG>RegistrarEvento</STRONG> solo está disponible en macros de datos.</span><span class="sxs-lookup"><span data-stu-id="af563-105">The <STRONG>LogEvent</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="af563-106">Valores</span><span class="sxs-lookup"><span data-stu-id="af563-106">Setting</span></span>

<span data-ttu-id="af563-107">La acción **RegistrarEvento** utiliza los siguientes argumentos.</span><span class="sxs-lookup"><span data-stu-id="af563-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af563-108">Argumento</span><span class="sxs-lookup"><span data-stu-id="af563-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="af563-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="af563-109">Required</span></span></p></th>
<th><p><span data-ttu-id="af563-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af563-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af563-111"><strong>Descripción</strong></span><span class="sxs-lookup"><span data-stu-id="af563-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="af563-112">No</span><span class="sxs-lookup"><span data-stu-id="af563-112">No</span></span></p></td>
<td><p><span data-ttu-id="af563-p101">Una expresión de cadena que describe la condición que desea registrar. La descripción no puede superar los 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="af563-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="af563-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af563-115">Remarks</span></span>

<span data-ttu-id="af563-p102">La acción **RegistrarEvento** puede utilizarse para escribir información de estado en la tabla de sistema **USysApplicationLog** que no puede utilizar la acción **[ProvocarError](raiseerror-macro-action.md)** para provocar un error. Por ejemplo, puede registrar los cambios realizados en un campo específico o usar los elementos que se escriben en la tabla **USysApplicationLog** para ayudarle a depurar la macro.</span><span class="sxs-lookup"><span data-stu-id="af563-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="af563-118">Si utiliza la acción **RegistrarEvento** para escribir en la tabla **USysApplicationLog**, la columna **Categoría** se establece automáticamente en **Usuario**.</span><span class="sxs-lookup"><span data-stu-id="af563-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="af563-119">Para ver la tabla **USysApplicationLog**, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="af563-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="af563-120">Haga clic en el menú **Archivo** y, a continuación, haga clic en **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="af563-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="af563-121">En el cuadro de diálogo **Opciones de Access**, haga clic en la pestaña **Base de datos actual**.</span><span class="sxs-lookup"><span data-stu-id="af563-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="af563-122">En la sección **Navegación**, haga clic en **Opciones de navegación**.</span><span class="sxs-lookup"><span data-stu-id="af563-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="af563-123">En el cuadro de diálogo **Opciones de navegación**, haga clic en **Mostrar objetos del sistema** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="af563-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="af563-124">Haga clic en **Aceptar** para descartar el cuadro de diálogo **Opciones de Access**.</span><span class="sxs-lookup"><span data-stu-id="af563-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

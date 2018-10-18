---
title: Source (propiedad, Recordset ADO)
TOCTitle: Source Property (ADO Recordset)
ms:assetid: 523ea81e-d011-8d87-436e-084b6eba0908
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249269(v=office.15)
ms:contentKeyID: 48544843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db44459bf3629f6cedfbee023b0be9161ed3bb14
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605264"
---
# <a name="source-property-ado-recordset"></a><span data-ttu-id="99ee3-102">Source (propiedad, Recordset ADO)</span><span class="sxs-lookup"><span data-stu-id="99ee3-102">Source Property (ADO Recordset)</span></span>


<span data-ttu-id="99ee3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="99ee3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="99ee3-104">Indica el origen de datos de un objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="99ee3-104">Indicates the data source for a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="99ee3-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="99ee3-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="99ee3-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="99ee3-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="99ee3-107">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="99ee3-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="99ee3-108">master</span><span class="sxs-lookup"><span data-stu-id="99ee3-108">master</span></span>

<span data-ttu-id="99ee3-109">Establece un valor de tipo **String** o una referencia al objeto [Command](command-object-ado.md); sólo devuelve un valor de tipo **String** que indica el origen del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="99ee3-109">Sets a **String** value or [Command](command-object-ado.md) object reference; returns only a **String** value that indicates the source of the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ee3-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99ee3-110">Remarks</span></span>

<span data-ttu-id="99ee3-111">Utilice la propiedad **Source** para especificar un origen de datos para un objeto **Recordset** mediante uno de los siguientes: una variable de objeto **Command**, una instrucción SQL, un procedimiento almacenado o un nombre de tabla.</span><span class="sxs-lookup"><span data-stu-id="99ee3-111">Use the **Source** property to specify a data source for a **Recordset** object using one of the following: a **Command** object variable, an SQL statement, a stored procedure, or a table name.</span></span>

<span data-ttu-id="99ee3-p101">Si se establece la propiedad **Source** en un objeto **Command**, la propiedad [ActiveConnection](activeconnection-property-ado.md) del objeto **Recordset** heredará el valor de la propiedad **ActiveConnection** para el objeto **Command** especificado. No obstante, la lectura de la propiedad **Source** no devuelve un objeto **Command**; por el contrario, devuelve la propiedad [CommandText](commandtext-property-ado.md) del objeto **Command** en el que se ha establecido la propiedad **Source**.</span><span class="sxs-lookup"><span data-stu-id="99ee3-p101">If you set the **Source** property to a **Command** object, the [ActiveConnection](activeconnection-property-ado.md) property of the **Recordset** object will inherit the value of the **ActiveConnection** property for the specified **Command** object. However, reading the **Source** property does not return a **Command** object; instead, it returns the [CommandText](commandtext-property-ado.md) property of the **Command** object to which you set the **Source** property.</span></span>

<span data-ttu-id="99ee3-114">Si la propiedad **Source** es una instrucción SQL, un procedimiento almacenado o un nombre de tabla, puede optimizar el rendimiento, se pasa el argumento *Options* adecuado con la llamada al método [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="99ee3-114">If the **Source** property is an SQL statement, a stored procedure, or a table name, you can optimize performance by passing the appropriate *Options* argument with the [Open](open-method-ado-recordset.md) method call.</span></span>

<span data-ttu-id="99ee3-115">La propiedad **Source** es de lectura y escritura para los objetos **Recordset** cerrados y de sólo lectura para los objetos **Recordset** abiertos.</span><span class="sxs-lookup"><span data-stu-id="99ee3-115">The **Source** property is read/write for closed **Recordset** objects and read-only for open **Recordset** objects.</span></span>


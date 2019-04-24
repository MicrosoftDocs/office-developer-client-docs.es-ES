---
title: Propiedad Recordset2. Filter (DAO)
TOCTitle: Filter Property
ms:assetid: 5b3b4e18-8af4-5acd-a129-513ba2d913d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194529(v=office.15)
ms:contentKeyID: 48545069
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053062
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 19f3c017aa5d4a353f3e832a3678d921565ea822
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307332"
---
# <a name="recordset2filter-property-dao"></a><span data-ttu-id="0a847-102">Propiedad Recordset2. Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="0a847-102">Recordset2.Filter property (DAO)</span></span>


<span data-ttu-id="0a847-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a847-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a847-104">Establece o devuelve un valor que determina los registros incluidos en un objeto **Recordset** abierto posteriormente (solo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0a847-104">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0a847-105">**String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0a847-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a847-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a847-106">Syntax</span></span>

<span data-ttu-id="0a847-107">*expresión* . Filter</span><span class="sxs-lookup"><span data-stu-id="0a847-107">*expression* .Filter</span></span>

<span data-ttu-id="0a847-108">*expresión* Expresión que devuelve un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="0a847-108">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a847-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a847-109">Remarks</span></span>

<span data-ttu-id="0a847-110">La configuración o el valor devuelto es un tipo de datos String que contiene la cláusula WHERE de una instrucción SQL sin la palabra reservada WHERE.</span><span class="sxs-lookup"><span data-stu-id="0a847-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="0a847-111">Use la propiedad **Filter** para aplicar un filtro a un objeto **Recordset** de tipo Dynaset, Snapshot o solo avance.</span><span class="sxs-lookup"><span data-stu-id="0a847-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="0a847-112">Puede usar la propiedad **Filter** para limitar los registros que se devuelven desde un objeto existente cuando un nuevo objeto **Recordset** se abre basado en un objeto **Recordset** existente.</span><span class="sxs-lookup"><span data-stu-id="0a847-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="0a847-113">Use el formato de fecha de Estados Unidos (mes-día-año) cuando filtre campos que contengan fechas, incluso si no está usando la versión en Estados Unidos del motor de base de datos de Microsoft Access (en cuyo caso debe reunir cualquier fecha concatenando cadenas, por ejemplo, strMonth & "-" _ aMP_ strDay & "-" & strYear).</span><span class="sxs-lookup"><span data-stu-id="0a847-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="0a847-114">De lo contrario, puede que no se filtren los datos de la forma esperada.</span><span class="sxs-lookup"><span data-stu-id="0a847-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="0a847-115">En mucho casos, es más rápido abrir un nuevo objeto **Recordset** mediante una instrucción SQL que incluya una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="0a847-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="0a847-116">Si establece la propiedad en una cadena concatenada con un valor distinto de Integer, y los parámetros del sistema especifican un carácter no-. S decimal como una coma (por ejemplo, strFilter = "PRICE \> " & lngPrice e lngPrice = 125, 50), se producirá un error cuando intente Abra el siguiente **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="0a847-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="0a847-117">Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="0a847-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


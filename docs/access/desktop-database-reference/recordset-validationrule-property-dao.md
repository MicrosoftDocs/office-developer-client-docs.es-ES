---
title: Recordset.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: c9250c13-18fe-1ff7-7846-7872c49a1e3b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823208(v=office.15)
ms:contentKeyID: 48547671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b4a15be2a1ef3ea31b078afb287ffa1f48dd232d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885048"
---
# <a name="recordsetvalidationrule-property-dao"></a><span data-ttu-id="e490f-102">Recordset.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e490f-102">Recordset.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="e490f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e490f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e490f-104">Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e490f-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e490f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e490f-105">Syntax</span></span>

<span data-ttu-id="e490f-106">*expresión* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="e490f-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="e490f-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="e490f-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e490f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e490f-108">Remarks</span></span>

<span data-ttu-id="e490f-p101">La configuración o los valores devueltos son de tipo **String** que describe una comparación en el formulario de una cláusula SQL WHERE sin la palabra reservada WHERE. Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e490f-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="e490f-p102">La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error capturable en tiempo de ejecución. El mensaje de error que se devuelve es el texto de la propiedad **ValidationText**, si se ha especificado, o el texto de la expresión especificada en **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="e490f-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="e490f-p103">Para un objeto **Recordset**, el uso de la propiedad **ValidationRule** es de solo lectura. Para un objeto **TableDef**, el uso de la propiedad **ValidationRule** depende del estado del objeto **TableDef**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e490f-p103">For a **Recordset** object, use of the **ValidationRule** property is read-only. For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e490f-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="e490f-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="e490f-117">Uso</span><span class="sxs-lookup"><span data-stu-id="e490f-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e490f-118">Tabla base</span><span class="sxs-lookup"><span data-stu-id="e490f-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="e490f-119">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="e490f-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e490f-120">Tabla vinculada</span><span class="sxs-lookup"><span data-stu-id="e490f-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="e490f-121">Sólo lectura</span><span class="sxs-lookup"><span data-stu-id="e490f-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e490f-122">La validación sólo se admite en las bases de datos que utilizan el motor de base de datos Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e490f-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="e490f-p104">La expresión de cadena especificada por la propiedad **ValidationRule** de un objeto **Field** puede referirse sólo a ese **Field**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar a **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.</span><span class="sxs-lookup"><span data-stu-id="e490f-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="e490f-p105">La propiedad **ValidationRule** de un objeto **Recordset** o **TableDef** puede hacer referencia a varios campos en esos objetos. Se aplican las restricciones comentadas anteriormente en este tema para el objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="e490f-p105">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="e490f-129">Para un objeto **Recordset** tipo Table, la propiedad **ValidationRule** hereda el valor de la propiedad **ValidationRule** del objeto **TableDef** que usa para crear un objeto **Recordset** tipo Table.</span><span class="sxs-lookup"><span data-stu-id="e490f-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e490f-130">Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strRule = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando el código intenta validar los datos.</span><span class="sxs-lookup"><span data-stu-id="e490f-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="e490f-131">Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="e490f-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>



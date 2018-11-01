---
title: Field2.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 006c9ce982aa98f28187d04fced12992d61548d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880057"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="7f429-102">Field2.ValidationRule Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7f429-102">Field2.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="7f429-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f429-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f429-p101">Establece o devuelve un valor que valida los datos de un campo cuando se cambia o agrega a una tabla (únicamente áreas de trabajo de Microsoft Access). **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7f429-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f429-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f429-106">Syntax</span></span>

<span data-ttu-id="7f429-107">*expresión* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="7f429-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="7f429-108">*expresión* Expresión que devuelve un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="7f429-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f429-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f429-109">Remarks</span></span>

<span data-ttu-id="7f429-p102">Los valores de configuración o valores devueltos son un String que describe una comparación en la forma de una cláusula SQL WHERE sin la palabra reservada WHERE. Para un objeto que todavía no está anexado a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7f429-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="7f429-p103">La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error capturable en tiempo de ejecución. El mensaje de error que se devuelve es el texto de la propiedad **ValidationText**, si se ha especificado, o el texto de la expresión especificada en **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="7f429-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="7f429-115">Para un objeto **Field2**, la utilización de la propiedad **ValidationRule** depende del objeto que contiene la colección **Fields** a la que está anexado el objeto **Field2**.</span><span class="sxs-lookup"><span data-stu-id="7f429-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7f429-116">Objeto anexado a</span><span class="sxs-lookup"><span data-stu-id="7f429-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="7f429-117">Uso</span><span class="sxs-lookup"><span data-stu-id="7f429-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f429-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="7f429-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="7f429-119">No admitido</span><span class="sxs-lookup"><span data-stu-id="7f429-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f429-120"><strong>Objeto QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="7f429-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7f429-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f429-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f429-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="7f429-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="7f429-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f429-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f429-124"><strong>Relación</strong></span><span class="sxs-lookup"><span data-stu-id="7f429-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="7f429-125">No admitido</span><span class="sxs-lookup"><span data-stu-id="7f429-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f429-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="7f429-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="7f429-127">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="7f429-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7f429-128">La validación sólo se admite en las bases de datos que utilizan el motor de base de datos Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="7f429-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="7f429-p104">La expresión de cadena que especifica la propiedad **ValidationRule** de un objeto **Field2** puede referirse sólo a ese **Field2**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field2** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar como **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.</span><span class="sxs-lookup"><span data-stu-id="7f429-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7f429-133">Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strRule = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando el código intenta validar los datos.</span><span class="sxs-lookup"><span data-stu-id="7f429-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="7f429-134">Esto se debe a que, durante la concatenación, el número se convertirá en una cadena que utiliza el carácter decimal predeterminado del sistema, y el motor de base de datos de Microsoft Access SQL sólo acepta caracteres decimales anglosajones.</span><span class="sxs-lookup"><span data-stu-id="7f429-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>



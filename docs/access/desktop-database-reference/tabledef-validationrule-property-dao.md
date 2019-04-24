---
title: Propiedad TableDef. ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314885"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="e9f77-102">Propiedad TableDef. ValidationRule (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9f77-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="e9f77-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9f77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9f77-104">Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e9f77-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f77-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9f77-105">Syntax</span></span>

<span data-ttu-id="e9f77-106">*expresión* . ValidationRule</span><span class="sxs-lookup"><span data-stu-id="e9f77-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="e9f77-107">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="e9f77-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f77-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e9f77-108">Remarks</span></span>

<span data-ttu-id="e9f77-p101">La configuración o los valores devueltos son de tipo **String** que describe una comparación en el formulario de una cláusula SQL WHERE sin la palabra reservada WHERE. Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e9f77-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="e9f77-p102">La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error en tiempo de ejecución capturable. El mensaje de error devuelto es el texto de la propiedad **ValidationText**, si se especifica, o el texto de la expresión especificada por **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="e9f77-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="e9f77-114">La validación sólo se admite para bases de datos que usan el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e9f77-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="e9f77-p103">La expresión de cadena especificada por la propiedad **ValidationRule** de un objeto **Field** puede referirse sólo a ese **Field**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar a **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.</span><span class="sxs-lookup"><span data-stu-id="e9f77-p103">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="e9f77-p104">La propiedad **ValidationRule** de un objeto **Recordset** o **TableDef** puede hacer referencia a varios campos de ese objeto. Son de aplicación las restricciones señaladas anteriormente en este tema para el objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="e9f77-p104">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="e9f77-p105">Para un objeto **TableDef** basado en una tabla vinculada, la propiedad **ValidationRule** hereda el valor de la propiedad **ValidationRule** de la tabla base subyacente. Si la tabla base subyacente no admite la validación, el valor de esta propiedad es una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="e9f77-p105">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table. If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="e9f77-123">Si establece la propiedad en una cadena concatenada con un valor que no sea entero, y los parámetros del sistema especifican un carácter no-. S decimal como una coma (por ejemplo, strRule = "Price &gt; " &amp; lngPrice e lngPrice = 125, 50), se producirá un error cuando el código intenta validar los datos.</span><span class="sxs-lookup"><span data-stu-id="e9f77-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="e9f77-124">Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="e9f77-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

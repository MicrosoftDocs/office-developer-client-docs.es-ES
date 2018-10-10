---
title: Filter (propiedad, ADO)
TOCTitle: Filter Property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 16c42ab071faea84db114a184ecd0db34bfd6074
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486427"
---
# <a name="filter-property-ado"></a><span data-ttu-id="546f1-102">Filter (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="546f1-102">Filter Property (ADO)</span></span>


<span data-ttu-id="546f1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="546f1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="546f1-104">Indica un filtro para datos en un objeto [ Recordset ](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="546f1-104">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="546f1-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="546f1-105">Settings and Return Values</span></span>

<span data-ttu-id="546f1-106">Establece o devuelve un valor de tipo **Variant** que puede contener uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="546f1-106">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="546f1-107">**Cadena de criterios**: una cadena compuesta por una o más cláusulas concatenadas mediante operadores **AND** u **OR**.</span><span class="sxs-lookup"><span data-stu-id="546f1-107">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="546f1-108">**Matriz de marcadores**: una matriz de valores de marcador exclusivos que señalan a registros del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="546f1-108">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="546f1-109">Un valor [FilterGroupEnum](filtergroupenum.md).</span><span class="sxs-lookup"><span data-stu-id="546f1-109">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="546f1-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="546f1-110">Remarks</span></span>

<span data-ttu-id="546f1-p101">Use la propiedad **Filter** para seleccionar registros de un objeto **Recordset**. El objeto **Recordset** filtrado se convierte en el cursor actual. Esto afecta a otras propiedades que devuelven valores basados en el cursor actual, como [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md) y [PageCount](pagecount-property-ado.md). Esto se debe a que al establecer la propiedad **Filter** en un valor específico, se moverá el registro actual al primer registro que satisfaga el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="546f1-p101">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor. Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md). This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="546f1-115">La cadena de criterios se compone de cláusulas con el formato *NombreCampo-Operador-valor* (por ejemplo, "LastName = 'Cervantes'").</span><span class="sxs-lookup"><span data-stu-id="546f1-115">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="546f1-116">Puede crear cláusulas compuestas concatenando cláusulas individuales con **AND** (por ejemplo, "LastName = 'Smith' AND FirstName = 'John'") u **OR** (por ejemplo, ").</span><span class="sxs-lookup"><span data-stu-id="546f1-116">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="546f1-117">Puede crear cláusulas compuestas concatenando cláusulas individuales con **AND** (por ejemplo, "LastName = 'Smith' AND FirstName = 'Juan'") u **OR** (por ejemplo, "LastName = 'Smith' OR LastName = 'Jones'").</span><span class="sxs-lookup"><span data-stu-id="546f1-117">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="546f1-118">Utilice las indicaciones siguientes para las cadenas de criterios:</span><span class="sxs-lookup"><span data-stu-id="546f1-118">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="546f1-119">*FieldName* debe ser un nombre de campo válido desde el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="546f1-119">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="546f1-120">Si el nombre de campo contiene espacios, debe ir entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="546f1-120">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="546f1-121">*Operador* debe ser uno de los siguientes: \<, \>, \<=, \>=, \< \>, = o **LIKE**.</span><span class="sxs-lookup"><span data-stu-id="546f1-121">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="546f1-122">*Valor* es el valor con el que se va a comparar los valores de campo (por ejemplo, 'Smith', \#24/8/95\#, 12.345 o $50.00).</span><span class="sxs-lookup"><span data-stu-id="546f1-122">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="546f1-123">Utilice comillas simples con las cadenas y signos de número (\#) con las fechas.</span><span class="sxs-lookup"><span data-stu-id="546f1-123">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="546f1-124">Con los números puede utilizar comas decimales, signos de dólar y notación científica.</span><span class="sxs-lookup"><span data-stu-id="546f1-124">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="546f1-125">Si el *operador* es **similar**, el *valor* puede usar caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="546f1-125">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="546f1-126">Sólo el asterisco (\*) y el signo de porcentaje (%) se permiten caracteres comodín y deben ser el último carácter en la cadena.</span><span class="sxs-lookup"><span data-stu-id="546f1-126">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="546f1-127">*Valor* no puede ser null.</span><span class="sxs-lookup"><span data-stu-id="546f1-127">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="546f1-p105">[!NOTA] Para incluir comillas sencillas (') en el filtro Valor, utilice dos comillas sencillas para representar una. Por ejemplo, para filtrar por O'Malley, la cadena de criterios debería ser "col1 = 'O''Malley'". Para incluir comillas sencillas al principio y al final del valor de filtrado, incluya la cadena entre signos de número (#). Por ejemplo, para filtrar por '1', la cadena de criterios debería ser "col1 = #'1'#".</span><span class="sxs-lookup"><span data-stu-id="546f1-p105">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one. For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'". To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#). For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span></P>



  - <span data-ttu-id="546f1-p106">No hay ninguna preferencia entre **AND** y **OR**. Las cláusulas se pueden agrupar entre paréntesis. Sin embargo, no es posible agrupar cláusulas unidas mediante **OR** y, a continuación, unir el grupo a otra cláusula mediante **AND**, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="546f1-p106">There is no precedence between **AND** and **OR**. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="546f1-135">Este filtro se construiría como</span><span class="sxs-lookup"><span data-stu-id="546f1-135">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="546f1-136">En una cláusula **LIKE** , puede utilizar un comodín al principio y al final del patrón (por ejemplo LastName Like '\*mit\*'), o sólo al final del patrón (por ejemplo LastName Like ' Smit\*').</span><span class="sxs-lookup"><span data-stu-id="546f1-136">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="546f1-137">Las constantes del filtro facilitan la resolución de conflictos de registros individuales durante el modo de actualización por lotes al permitir ver, por ejemplo, sólo aquellos registros afectados durante la última llamada al método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="546f1-137">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="546f1-p107">El establecimiento de la propiedad **Filter** por sí misma puede dar lugar a un error a causa de un conflicto con los datos subyacentes (por ejemplo, en el caso de que un registro ya haya sido eliminado por otro usuario). En este caso, el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) pero no detiene la ejecución del programa. Solo se produce un error en tiempo de ejecución si existen conflictos en todos los registros solicitados. Use la propiedad [Status](status-property-ado-recordset.md) para buscar registros con conflictos.</span><span class="sxs-lookup"><span data-stu-id="546f1-p107">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user). In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="546f1-142">El establecimiento de la propiedad **Filter** en una cadena de longitud cero ("") tiene el mismo efecto que el uso de la constante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="546f1-142">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="546f1-p108">Siempre que se establece la propiedad **Filter**, la posición del registro actual se mueve al primer registro del subconjunto filtrado de registros del objeto **Recordset**. Igualmente, cuando se borra la propiedad **Filter**, la posición del registro actual se mueve al primer registro del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="546f1-p108">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**. Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="546f1-145">Vea la propiedad [Bookmark](bookmark-property-ado.md) para obtener una explicación de los valores de marcador a partir de los que se puede construir una matriz para utilizarla con la propiedad **Filter**.</span><span class="sxs-lookup"><span data-stu-id="546f1-145">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="546f1-146">Sólo los **filtros** con el formato de las cadenas de criterios (por ejemplo, FechaPedido \> ' 12/31/1999 ') afectan al contenido de un **objeto Recordset**de persistentes.</span><span class="sxs-lookup"><span data-stu-id="546f1-146">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="546f1-147">Los **filtros** creados con una matriz de **marcadores** o mediante un valor de **FilterGroupEnum** no afectarán al contenido del objeto Recordset persistente.</span><span class="sxs-lookup"><span data-stu-id="546f1-147">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="546f1-148">Estas reglas se aplican a los objetos **Recordset** creados con cursores cliente o servidor.</span><span class="sxs-lookup"><span data-stu-id="546f1-148">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>


> [!NOTE]
> <P><span data-ttu-id="546f1-p110">[!NOTA] Cuando se aplica la marca <STRONG>adFilterPendingRecords</STRONG> a un objeto <STRONG>Recordset</STRONG> filtrado y modificado en el modo de actualización por lotes, el objeto <STRONG>Recordset</STRONG> resultante estará vacío si el filtrado se ha basado en el campo clave de una tabla de una única clave y la modificación se ha realizado en los valores del campo clave. El objeto <STRONG>Recordset</STRONG> resultante no estará vacío si se cumple una de las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="546f1-p110">When you apply the <STRONG>adFilterPendingRecords</STRONG> flag to a filtered and modified <STRONG>Recordset</STRONG> in the batch update mode, the resultant <STRONG>Recordset</STRONG> is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values. The resultant <STRONG>Recordset</STRONG> will be non-empty if one of the following is true:</span></span></P>



  - <span data-ttu-id="546f1-151">El filtrado se ha basado en campos sin clave de una tabla con una única clave.</span><span class="sxs-lookup"><span data-stu-id="546f1-151">The filtering was based on non-key fields in a single-keyed table.</span></span>

  - <span data-ttu-id="546f1-152">El filtrado se ha basado en cualquier campo de una tabla con varias claves.</span><span class="sxs-lookup"><span data-stu-id="546f1-152">The filtering was based on any fields in a multiple-keyed table.</span></span>

  - <span data-ttu-id="546f1-153">Las modificaciones se han realizado en campos sin clave de una tabla con una única clave.</span><span class="sxs-lookup"><span data-stu-id="546f1-153">Modifications were made on non-key fields in a single-keyed table.</span></span>

  - <span data-ttu-id="546f1-154">Las modificaciones se han realizado en cualquier campo de una tabla con varias claves.</span><span class="sxs-lookup"><span data-stu-id="546f1-154">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="546f1-p111">En la siguiente tabla se resumen los efectos de **adFilterPendingRecords** sobre diferentes combinaciones de filtrado y modificaciones. En la columna de la izquierda se muestran las posibles modificaciones; éstas se pueden realizar en cualquiera de los campos sin clave, en el campo clave de una tabla con una única clave o en cualquiera de los campos clave de una tabla con varias claves. En la fila superior se muestra el criterio de filtrado; éste puede basarse en cualquiera de los campos sin clave, en el campo clave de una tabla con una única clave o en cualquiera de los campos clave de una tabla con varias claves. En las celdas de intersección se muestran los resultados: + significa que la aplicación de **adFilterPendingRecords** da lugar a un objeto **Recordset** no vacío; **-** significa un objeto **Recordset** vacío.</span><span class="sxs-lookup"><span data-stu-id="546f1-p111">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications. The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table. The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table. The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p><span data-ttu-id="546f1-159">Sin clave</span><span class="sxs-lookup"><span data-stu-id="546f1-159">Non keys</span></span></p></th>
<th><p><span data-ttu-id="546f1-160">Clave única</span><span class="sxs-lookup"><span data-stu-id="546f1-160">Single Key</span></span></p></th>
<th><p><span data-ttu-id="546f1-161">Varias claves</span><span class="sxs-lookup"><span data-stu-id="546f1-161">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="546f1-162">Sin clave</span><span class="sxs-lookup"><span data-stu-id="546f1-162">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="546f1-163">Clave única</span><span class="sxs-lookup"><span data-stu-id="546f1-163">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="546f1-164">N/A</span><span class="sxs-lookup"><span data-stu-id="546f1-164">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="546f1-165">Varias claves</span><span class="sxs-lookup"><span data-stu-id="546f1-165">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="546f1-166">N/D</span><span class="sxs-lookup"><span data-stu-id="546f1-166">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>


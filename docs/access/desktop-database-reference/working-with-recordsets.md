---
title: Trabajar con conjuntos de registros
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d4b877b680c80a10067e19065facd4ce9e4819d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305979"
---
# <a name="working-with-recordsets"></a><span data-ttu-id="23a6c-102">Trabajo con conjuntos de registros</span><span class="sxs-lookup"><span data-stu-id="23a6c-102">Working with Recordsets</span></span>

<span data-ttu-id="23a6c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23a6c-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="23a6c-p101">El objeto **Recordset** tiene características integradas para reorganizar el orden de los datos en el conjunto de resultados, para buscar un registro concreto según los criterios especificados e, incluso, para optimizar aquellas operaciones de búsqueda mediante índices. La disponibilidad de uso de estas características depende del proveedor y, en algunos casos, como en el de la propiedad [Index](index-property-ado.md), de la estructura del propio origen de datos.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p101">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes. Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="23a6c-106">Organizar datos</span><span class="sxs-lookup"><span data-stu-id="23a6c-106">Arranging data</span></span>

<span data-ttu-id="23a6c-p102">A menudo, la manera más eficaz de ordenar los datos en un objeto **Recordset** consiste en especificar una cláusula ORDER BY en el comando SQL usado para devolver los resultados. Sin embargo, podría ser necesario cambiar el orden de los datos en un objeto **Recordset** que ya se ha creado. Puede usar la propiedad **Sort** para establecer el orden en el que se recorren las filas de un objeto **Recordset**. Además, la propiedad **Filter** determina cuáles son las filas a las que se puede tener acceso en ese recorrido.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p102">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it. However, you might need to change the order of the data in a **Recordset** that has already been created. You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed. Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="23a6c-p103">La propiedad **Sort** establece o devuelve un valor **String** que indica los nombres de campos del objeto **Recordset** por los que se debe ordenar. Cada nombre se separa por una coma, seguida opcionalmente de un espacio y la palabra clave **ASC** (que ordena el campo de forma ascendente) o **DESC** (que ordena el campo de forma descendente). De forma predeterminada, si no se especifica ninguna palabra clave, el campo se ordena de forma ascendente.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p103">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order). By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="23a6c-114">La operación de ordenación es eficaz, ya que los datos no se reorganizan físicamente, sino que el acceso a ellos se realiza simplemente en el orden especificado por un índice.</span><span class="sxs-lookup"><span data-stu-id="23a6c-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="23a6c-p104">La propiedad **Sort** requiere que la propiedad [CursorLocation](cursorlocation-property-ado.md) se establezca en el valor **adUseClient**. Si no existe ningún índice, se creará uno temporal para cada campo especificado en la propiedad **Sort**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p104">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="23a6c-p105">Si se establece la propiedad **Sort** en una cadena vacía, las filas se restablecerán a su orden original y se eliminarán los índices temporales. No se eliminarán los índices existentes.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p105">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="23a6c-119">Suponga que **Recordset** contiene tres campos denominados *firstName*, *middleInitial* y *lastName*.</span><span class="sxs-lookup"><span data-stu-id="23a6c-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="23a6c-120">Establezca la **propiedad Sort** en la cadena  "", que ordenará el conjunto de registros por apellidos en orden descendente y, a continuación, por nombre en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="23a6c-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="23a6c-121">La posible inicial media se omite.</span><span class="sxs-lookup"><span data-stu-id="23a6c-121">The middle initial is ignored.</span></span>

<span data-ttu-id="23a6c-p107">Las referencias a los campos en una cadena de criterios de ordenación no se pueden denominar "ASC" o "DESC", ya que esos nombres entran en conflicto con las palabras clave **ASC** y **DESC**. Use un alias para un campo con un nombre conflictivo mediante la palabra clave **AS** en la consulta que devuelve el objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p107">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="23a6c-124">Para obtener más detalles sobre cómo filtrar los objetos **Recordset**, vea Filtrar los resultados más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="23a6c-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="23a6c-125">Buscar un registro específico</span><span class="sxs-lookup"><span data-stu-id="23a6c-125">Finding a specific record</span></span>

<span data-ttu-id="23a6c-p108">ADO proporciona los métodos [Find](find-method-ado.md) y [Seek](seek-method-ado.md) para buscar un registro determinado en un objeto **Recordset**. Diversos proveedores admiten el método **Find**, pero se limita a criterios de búsqueda único. El método **Seek** permite la búsqueda con varios criterios, pero el número de proveedores que lo admiten es reducido.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p108">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**. The **Find** method is supported by a variety of providers but is limited to a single search criterion. The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="23a6c-p109">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties. You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property. This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**. Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose. Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p109">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties. You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property. This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**. Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose. Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="23a6c-p110">The **Find** method quickly locates a value within a column (field) of a **Recordset**. You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p110">The **Find** method quickly locates a value within a column (field) of a **Recordset**. You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="23a6c-p111">El método **Find** limita la búsqueda al contenido de un campo. El método **Seek** requiere un índice y tiene también otras limitaciones. Si es necesario buscar en varios campos que no constituyan un índice, o si su proveedor no admite índices, puede limitar los resultados mediante la propiedad **Filter** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p111">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

### <a name="find"></a><span data-ttu-id="23a6c-139">Buscar</span><span class="sxs-lookup"><span data-stu-id="23a6c-139">Find</span></span>

<span data-ttu-id="23a6c-p112">El método **Find** busca en un objeto **Recordset** la fila que cumple un criterio especificado. Opcionalmente, es posible especificar la dirección de la búsqueda, la fila inicial y el desplazamiento desde ésta. Si se cumple el criterio, la posición de la fila actual se establece en el registro encontrado; de lo contrario, se establece al final o al principio del objeto **Recordset**, según la dirección de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p112">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="23a6c-p113">Sólo se puede especificar un único nombre de columna para el criterio. Es decir, este método no admite búsquedas en varias columnas.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p113">Only a single-column name may be specified for the criterion. In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="23a6c-145">El operador de comparación para el criterio puede ser **\>** " " (mayor que), \*\*\<** " (menor que), "=" (igual), " =" (mayor o igual que), " =" (menor o igual que), " (no es igual) o \> \< \< \> "LIKE" (coincidencia de patrones).</span><span class="sxs-lookup"><span data-stu-id="23a6c-145">The comparison operator for the criterion may be "**\>**" (greater than), "\*\*\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="23a6c-146">El valor del criterio puede ser una cadena, un número de punto flotante o una fecha.</span><span class="sxs-lookup"><span data-stu-id="23a6c-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="23a6c-147">Los valores de cadena se delimitan con comillas simples o marcas " " (signo de \# número) (por ejemplo, "state = 'WA'" o "state = \# \# WA").</span><span class="sxs-lookup"><span data-stu-id="23a6c-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="23a6c-148">Los valores de fecha se delimitan con marcas " " (signo de \# número) (por ejemplo, "fecha de inicio \_ \> \# 22/7/97"). \#</span><span class="sxs-lookup"><span data-stu-id="23a6c-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="23a6c-p115">Si el operador de comparación es "like", el valor de cadena puede contener un asterisco (\*) para que se busque una o varias apariciones de cualquier carácter o subcadena. Por ejemplo, "state like 'M\*'" encuentra Maine y Massachusetts.También se pueden utilizar asteriscos inicial y final para buscar una subcadena incluida en los valores. Por ejemplo, "state like '\*as\*' encuentra Alaska, Arkansas y Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p115">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="23a6c-p116">Se pueden utilizar asteriscos sólo al final de la cadena; o bien, tanto al principio como al final de la cadena, como se ha indicado anteriormente. No se puede utilizar el asterisco como comodín inicial ('\*str') o comodín incrustado ('s\*r'). De lo contrario, se generará un error.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p116">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r'). This will cause an error.</span></span>

### <a name="seek-and-index"></a><span data-ttu-id="23a6c-156">Seek e Index</span><span class="sxs-lookup"><span data-stu-id="23a6c-156">Seek and Index</span></span>

<span data-ttu-id="23a6c-p117">Use el método **Seek** junto con la propiedad **Index** si el proveedor subyacente admite índices en el objeto **Recordset**. Use el método [Supports](supports-method-ado.md)**(adSeek)** para determinar si el proveedor subyacente admite **Seek**, y el método **Supports(adIndex)** para determinar si el proveedor admite índices. Por ejemplo, el [proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) admite **Seek** e **Index**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p117">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="23a6c-p118">Si **Seek** no encuentra la fila deseada, no se produce ningún error y la fila se coloca al final del objeto **Recordset**. Establezca la propiedad **Index** en el índice deseado antes de ejecutar este método.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p118">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="23a6c-p119">Este método se puede usar únicamente con cursores de servidor. Seek no se admite cuando el valor de la propiedad **CursorLocation** del objeto [Recordset](cursorlocation-property-ado.md) es **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p119">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="23a6c-164">Este método se puede usar únicamente cuando el objeto **Recordset** se abrió con el valor [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="23a6c-165">Filtrar los resultados</span><span class="sxs-lookup"><span data-stu-id="23a6c-165">Filtering the results</span></span>

<span data-ttu-id="23a6c-p120">El método **Find** limita la búsqueda al contenido de un campo. El método **Seek** requiere un índice y tiene también otras limitaciones. Si es necesario buscar en varios campos que no constituyan un índice, o si su proveedor no admite índices, puede limitar los resultados mediante la propiedad **Filter** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p120">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="23a6c-p121">Use la propiedad **Filter** para ocultar selectivamente los registros de un objeto **Recordset**. El objeto **Recordset** filtrado se convierte en el cursor actual; es decir, los registros que no cumplan los criterios de **Filter** no están disponibles en el objeto **Recordset** hasta que se quite **Filter**. Otras propiedades que devuelven valores según el cursor actual, como **AbsolutePosition**, **AbsolutePage**, **RecordCount** y **PageCount**, también se ven afectadas. Esto se debe a que, al establecer la propiedad **Filter** en un valor específico, el registro actual pasa a ser el primer registro que cumple el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p121">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed. Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**. This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="23a6c-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="23a6c-176">[!NOTA] Cuando se conocen los datos que se desean seleccionar, normalmente es más eficiente abrir un objeto **Recordset** con una instrucción SQL que filtra, de hecho, el conjunto de resultados, en vez de utilizar la propiedad **Filter**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-176">When you know the data you want to select, it is usually more efficient to open a **Recordset** with a SQL statement that effectively filters the result set, rather than relying on the **Filter** property.</span></span>

<span data-ttu-id="23a6c-p123">Para quitar un filtro de un objeto **Recordset**, use la constante **adFilterNone**. El establecimiento de la propiedad **Filter** en una cadena de longitud cero ("") tiene el mismo efecto que el uso de la constante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p123">To remove a filter from a **Recordset**, use the **adFilterNone** constant. Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

### <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="23a6c-179">Filtrado con una cadena de criterios</span><span class="sxs-lookup"><span data-stu-id="23a6c-179">Filtering with a criteria string</span></span>

<span data-ttu-id="23a6c-180">La cadena de criterios está hecha de cláusulas con el formato *FieldName Operator Value* (por ejemplo, "LastName = 'Smith'").</span><span class="sxs-lookup"><span data-stu-id="23a6c-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="23a6c-181">Puede crear cláusulas compuestas concatenando cláusulas individuales con AND (por ejemplo, "LastName = 'Smith' AND FirstName = 'John'") y OR (por ejemplo, ).</span><span class="sxs-lookup"><span data-stu-id="23a6c-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="23a6c-182">Puede crear cláusulas compuestas concatenando cláusulas individuales con AND (por ejemplo, "LastName = 'Smith' AND FirstName = 'John'") y OR (por ejemplo, "LastName = 'Smith' OR LastName = 'Jones'").</span><span class="sxs-lookup"><span data-stu-id="23a6c-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="23a6c-183">Utilice las siguientes directrices para las cadenas de criterios:</span><span class="sxs-lookup"><span data-stu-id="23a6c-183">Use the following guidelines for criteria strings:</span></span>

- <span data-ttu-id="23a6c-p125">*NombreCampo* debe ser un nombre de campo válido del objeto **Recordset**. Si el nombre de campo contiene espacios, debe ir entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p125">*FieldName* must be a valid field name from the **Recordset**. If the field name contains spaces, you must enclose the name in square brackets.</span></span>

- <span data-ttu-id="23a6c-186">*El* operador debe ser uno de los siguientes: \< , = , \> \< \> =, = , = o \< \> LIKE.</span><span class="sxs-lookup"><span data-stu-id="23a6c-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

- <span data-ttu-id="23a6c-187">*El* valor es el valor con el que comparará los valores de campo (por ejemplo, 'Smith', \# 24/8/95, \# 12,345 o 50,00 $).</span><span class="sxs-lookup"><span data-stu-id="23a6c-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="23a6c-188">Use comillas simples (') con cadenas y signos de kilo ( \# ) con fechas.</span><span class="sxs-lookup"><span data-stu-id="23a6c-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="23a6c-189">Por lo que respecta a los números, puede utilizar separadores decimales, signos de dólar y notación científica.</span><span class="sxs-lookup"><span data-stu-id="23a6c-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="23a6c-190">Si *Operador* es LIKE, *Valor* puede utilizar caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="23a6c-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="23a6c-191">Solo el asterisco ( \* ) y el signo de porcentaje (%) se permiten caracteres comodín y deben ser el último carácter de la cadena.</span><span class="sxs-lookup"><span data-stu-id="23a6c-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="23a6c-192">*Valor* no puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="23a6c-192">*Value* cannot be null.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="23a6c-193">Para incluir comillas simples (') en *Valor*, utilice dos comillas simples para representar una.</span><span class="sxs-lookup"><span data-stu-id="23a6c-193">To include single quotation marks (') in the filter *Value*, use two single quotation marks to represent one.</span></span> <span data-ttu-id="23a6c-194">Por ejemplo, para filtrar por *O'Malley,* la cadena de criterios debe ser "col1 = 'O''Malley'".</span><span class="sxs-lookup"><span data-stu-id="23a6c-194">For example, to filter on *O'Malley*, the criteria string should be "col1 = 'O''Malley'".</span></span> 
  > 
  > <span data-ttu-id="23a6c-195">Para incluir comillas simples al principio y al final del valor de filtro, ponga la cadena entre signos de número (#).</span><span class="sxs-lookup"><span data-stu-id="23a6c-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="23a6c-196">Por ejemplo, para filtrar por *"1",* la cadena de criterios debe ser "col1 = #'1'#".</span><span class="sxs-lookup"><span data-stu-id="23a6c-196">For example, to filter on *'1'*, the criteria string should be "col1 = #'1'#".</span></span>

<span data-ttu-id="23a6c-p129">No se aplica ningún orden de prioridad entre AND y OR. Las cláusulas se pueden agrupar entre paréntesis. Sin embargo, no puede agrupar cláusulas unidas por un operador OR y, a continuación, unir el grupo a otra cláusula con un operador AND, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="23a6c-p129">There is no precedence between AND and OR. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="23a6c-200">En su lugar, debería crear el filtro del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="23a6c-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="23a6c-201">En una cláusula LIKE, puede usar un carácter comodín al principio y al final del patrón (por ejemplo, LastName Like ' mit ') o solo al final del patrón (por ejemplo, ) o solo al final del patrón \* \* (por ejemplo, LastName Like 'Smit'). \*</span><span class="sxs-lookup"><span data-stu-id="23a6c-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

### <a name="filtering-with-a-constant"></a><span data-ttu-id="23a6c-202">Filtrado con una constante</span><span class="sxs-lookup"><span data-stu-id="23a6c-202">Filtering with a constant</span></span>

<span data-ttu-id="23a6c-203">Las constantes siguientes están disponibles para filtrar objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="23a6c-204">Constante</span><span class="sxs-lookup"><span data-stu-id="23a6c-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="23a6c-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="23a6c-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23a6c-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="23a6c-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="23a6c-207">Filtra de modo que sólo se vean los registros afectados por la última llamada a <strong>Delete</strong>, <strong>Resynch</strong>, <strong>UpdateBatch</strong> o <strong>CancelBatch</strong>.</span><span class="sxs-lookup"><span data-stu-id="23a6c-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23a6c-208"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="23a6c-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="23a6c-209">Filtra de modo que se vean los registros que no superaron la última actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="23a6c-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23a6c-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="23a6c-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="23a6c-211">Filtra de modo que se vean los registros almacenados en la memoria caché actual, es decir, los resultados de la última llamada para recuperar registros de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="23a6c-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23a6c-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="23a6c-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="23a6c-213">Quita el filtro actual de modo que se puedan ver todos los registros.</span><span class="sxs-lookup"><span data-stu-id="23a6c-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23a6c-214"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="23a6c-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="23a6c-215">Filtra de modo que se vean sólo los registros que han cambiado, pero que aún no se han enviado al servidor.</span><span class="sxs-lookup"><span data-stu-id="23a6c-215">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="23a6c-216">Sólo se aplica al modo de actualización de proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="23a6c-216">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="23a6c-217">Las constantes de filtro facilitan la resolución de conflictos de registros individuales durante el modo de actualización de proceso por lotes al permitir ver, por ejemplo, sólo aquellos registros que se vieron afectados durante la última llamada al método **UpdateBatch**, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="23a6c-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

### <a name="filtering-with-bookmarks"></a><span data-ttu-id="23a6c-218">Filtrado con marcadores</span><span class="sxs-lookup"><span data-stu-id="23a6c-218">Filtering with bookmarks</span></span>

<span data-ttu-id="23a6c-p131">Por último, puede pasar una matriz Variant de marcadores a la propiedad **Filter**. El cursor resultante contendrá solo aquellos registros cuyo marcador se pasó a la propiedad. En el ejemplo de código siguiente, se crea una matriz de marcadores a partir de los registros de un objeto **Recordset** que tienen una "B" en el campo *ProductName*. A continuación, se pasa la matriz a la propiedad **Filter** y se muestra información acerca del objeto **Recordset** filtrado resultante.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p131">Finally, you can pass a variant array of bookmarks to the **Filter** property. The resulting cursor will contain only those records whose bookmark was passed in to the property. The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field. It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="23a6c-223">Creación de un clon de un conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="23a6c-223">Creating a clone of a Recordset</span></span>

<span data-ttu-id="23a6c-p132">Use el método **Clone** para crear varios objetos **Recordset** duplicados, sobre todo si desea mantener más de un registro actual en un conjunto determinado de registros. El método **Clone** es más eficaz que crear y abrir un nuevo objeto **Recordset** con la misma definición que el original.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p132">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="23a6c-p133">El registro actual de un clon recién creado se establece originalmente en el primer registro. El puntero del registro actual de un objeto **Recordset** clonado no está sincronizado con el original ni viceversa. Es posible navegar independientemente en cada objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p133">The current record of a newly created clone is originally set to the first record. The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa. You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="23a6c-p134">Los cambios realizados en un objeto **Recordset** se ven en todos sus duplicados, independientemente del tipo de cursor. Sin embargo, después de ejecutar [Requery](requery-method-ado.md) en el objeto **Recordset** original, los duplicados ya no estarán sincronizados con el original.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p134">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="23a6c-231">Al cerrar el objeto **Recordset** original, no se cierran sus copias; como tampoco se cierra el original ni ninguna de las demás copias al cerrarse una copia.</span><span class="sxs-lookup"><span data-stu-id="23a6c-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="23a6c-p135">Se puede clonar un objeto **Recordset** sólo si admite marcadores. Los valores de los marcadores son intercambiables; es decir, una referencia de marcador de un objeto **Recordset** hace referencia al mismo registro en todos sus clones.</span><span class="sxs-lookup"><span data-stu-id="23a6c-p135">You can clone a **Recordset** object only if it supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>


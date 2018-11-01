---
title: Trabajar con conjuntos de registros
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d57f05905aa0f79c1a72638e70ede8bdabf73b8f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883690"
---
# <a name="working-with-recordsets"></a>Trabajar con conjuntos de registros


**Se aplica a**: Access 2013, Office 2013 

El objeto **Recordset** tiene características integradas para reorganizar el orden de los datos en el conjunto de resultados, para buscar un registro concreto según los criterios especificados e, incluso, para optimizar aquellas operaciones de búsqueda mediante índices. La disponibilidad de uso de estas características depende del proveedor y, en algunos casos, como en el de la propiedad [Index](index-property-ado.md), de la estructura del propio origen de datos.

## <a name="arranging-data"></a>Organizar los datos

A menudo, la manera más eficaz de ordenar los datos en un objeto **Recordset** consiste en especificar una cláusula ORDER BY en el comando SQL usado para devolver los resultados. Sin embargo, podría ser necesario cambiar el orden de los datos en un objeto **Recordset** que ya se ha creado. Puede usar la propiedad **Sort** para establecer el orden en el que se recorren las filas de un objeto **Recordset**. Además, la propiedad **Filter** determina cuáles son las filas a las que se puede tener acceso en ese recorrido.

La propiedad **Sort** establece o devuelve un valor **String** que indica los nombres de campos del objeto **Recordset** por los que se debe ordenar. Cada nombre se separa por una coma, seguida opcionalmente de un espacio y la palabra clave **ASC** (que ordena el campo de forma ascendente) o **DESC** (que ordena el campo de forma descendente). De forma predeterminada, si no se especifica ninguna palabra clave, el campo se ordena de forma ascendente.

La operación de ordenación es eficaz, ya que los datos no se reorganizan físicamente, sino que el acceso a ellos se realiza simplemente en el orden especificado por un índice.

La propiedad **Sort** requiere que la propiedad [CursorLocation](cursorlocation-property-ado.md) se establezca en el valor **adUseClient**. Si no existe ningún índice, se creará uno temporal para cada campo especificado en la propiedad **Sort**.

Si se establece la propiedad **Sort** en una cadena vacía, las filas se restablecerán a su orden original y se eliminarán los índices temporales. No se eliminarán los índices existentes.

Supongamos que un **objeto Recordset** contiene tres campos denominados *firstName*, *middleInitial*y *LastName (apellidos)*. Establezca la propiedad **Sort** en la cadena "", que ordenará el **conjunto de registros** por apellidos en orden descendente y, a continuación, por nombre en orden ascendente. La posible inicial media se omite.

Las referencias a los campos en una cadena de criterios de ordenación no se pueden denominar "ASC" o "DESC", ya que esos nombres entran en conflicto con las palabras clave **ASC** y **DESC**. Use un alias para un campo con un nombre conflictivo mediante la palabra clave **AS** en la consulta que devuelve el objeto **Recordset**.

Para obtener más detalles sobre cómo filtrar los objetos **Recordset**, vea Filtrar los resultados más adelante en este tema.

## <a name="finding-a-specific-record"></a>Buscar un registro específico

ADO proporciona los métodos [Find](find-method-ado.md) y [Seek](seek-method-ado.md) para buscar un registro determinado en un objeto **Recordset**. Diversos proveedores admiten el método **Find**, pero se limita a criterios de búsqueda único. El método **Seek** permite la búsqueda con varios criterios, pero el número de proveedores que lo admiten es reducido.

Los índices de campos pueden mejorar mucho el rendimiento del método **Find** y de las propiedades **Sort** y ** Filter** del objeto **Recordset**. Puede crear un índice interno para un objeto **Field** si establece su propiedad dinámica [Optimize](optimize-property-dynamic-ado.md). Esta propiedad se agrega a la colección **Properties** del objeto **Field** al establecer la propiedad [CursorLocation](cursorlocation-property-ado.md) en el valor **adUseClient**. Recuerde que este índice es interno respecto a ADO, es decir, no se puede obtener acceso a él ni usarlo para ningún otro fin. Además, este índice es distinto de la propiedad [Index](index-property-ado.md) del objeto **Recordset**.

El método **Find** busca rápidamente un valor en una columna (campo) de un objeto **Recordset**. La velocidad de operación de este método**** en una columna se puede mejorar, a menudo, mediante la propiedad **Optimize** para crear un índice en esa columna.

El método **Find** limita la búsqueda al contenido de un campo. El método **Seek** requiere un índice y tiene también otras limitaciones. Si es necesario buscar en varios campos que no constituyan un índice, o si su proveedor no admite índices, puede limitar los resultados mediante la propiedad **Filter** del objeto **Recordset**.

## <a name="find"></a>Find

El método **Find** busca en un objeto **Recordset** la fila que cumple un criterio especificado. Opcionalmente, es posible especificar la dirección de la búsqueda, la fila inicial y el desplazamiento desde ésta. Si se cumple el criterio, la posición de la fila actual se establece en el registro encontrado; de lo contrario, se establece al final o al principio del objeto **Recordset**, según la dirección de búsqueda.

Sólo se puede especificar un único nombre de columna para el criterio. Es decir, este método no admite búsquedas en varias columnas.

El operador de comparación para el criterio puede ser "**\>**"(mayor que),"**\<**"(menor que), "=" (igual a),"\>=" (mayor o igual que), "\<=" (menor o igual que), "\<\>" (no igual a), o "LIKE" (coincidencia de modelos).

El valor del criterio puede ser una cadena, un número de punto flotante o una fecha. Valores de cadena se delimitan con comillas simples o "\#" (signo de número) marca (por ejemplo, "estado = 'WA'" o "estado = \#WA\#"). Los valores de fecha se delimitan con "\#" (signo de número) marca (por ejemplo, "iniciar\_fecha \> \#22/7/97\#").

Si el operador de comparación es "like", el valor de cadena puede contener un asterisco (\*) para que se busque una o varias apariciones de cualquier carácter o subcadena. Por ejemplo, "state like 'M\*'" encuentra Maine y Massachusetts.También se pueden utilizar asteriscos inicial y final para buscar una subcadena incluida en los valores. Por ejemplo, "state like '\*as\*' encuentra Alaska, Arkansas y Massachusetts.

Se pueden utilizar asteriscos sólo al final de la cadena; o bien, tanto al principio como al final de la cadena, como se ha indicado anteriormente. No se puede utilizar el asterisco como comodín inicial ('\*str') o comodín incrustado ('s\*r'). De lo contrario, se generará un error.

## <a name="seek-and-index"></a>Seek e Index

Use el método **Seek** junto con la propiedad **Index** si el proveedor subyacente admite índices en el objeto **Recordset**. Use el método [Supports](supports-method-ado.md)**(adSeek)** para determinar si el proveedor subyacente admite **Seek**, y el método **Supports(adIndex)** para determinar si el proveedor admite índices. Por ejemplo, el [proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) admite **Seek** e **Index**.

Si **Seek** no encuentra la fila deseada, no se produce ningún error y la fila se coloca al final del objeto **Recordset**. Establezca la propiedad **Index** en el índice deseado antes de ejecutar este método.

Este método se puede usar únicamente con cursores de servidor. Seek no se admite cuando el valor de la propiedad **CursorLocation** del objeto [Recordset](cursorlocation-property-ado.md) es **adUseClient**.

Este método se puede usar únicamente cuando el objeto **Recordset** se abrió con el valor [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.

## <a name="filtering-the-results"></a>Filtrar los resultados

El método **Find** limita la búsqueda al contenido de un campo. El método **Seek** requiere un índice y tiene también otras limitaciones. Si es necesario buscar en varios campos que no constituyan un índice, o si su proveedor no admite índices, puede limitar los resultados mediante la propiedad **Filter** del objeto **Recordset**.

Use la propiedad **Filter** para ocultar selectivamente los registros de un objeto **Recordset**. El objeto **Recordset** filtrado se convierte en el cursor actual; es decir, los registros que no cumplan los criterios de **Filter** no están disponibles en el objeto **Recordset** hasta que se quite **Filter**. Otras propiedades que devuelven valores según el cursor actual, como **AbsolutePosition**, **AbsolutePage**, **RecordCount** y **PageCount**, también se ven afectadas. Esto se debe a que, al establecer la propiedad **Filter** en un valor específico, el registro actual pasa a ser el primer registro que cumple el nuevo valor.

La propiedad **Filter** toma un argumento Variant. Este valor representa uno de los tres métodos para utilizar esta**** propiedad: una cadena de criterio, una constante **FilterGroupEnum** o una matriz de marcadores. Para obtener más información, vea Filtrar por una cadena de criterios, Filtrar por una constante y Filtrar por marcadores, más adelante en este mismo tema.


> [!NOTE]
> <P>[!NOTA] Cuando se conocen los datos que se desean seleccionar, normalmente es más eficiente abrir un objeto <STRONG>Recordset</STRONG> con una instrucción SQL que filtra, de hecho, el conjunto de resultados, en vez de utilizar la propiedad <STRONG>Filter</STRONG>.</P>



Para quitar un filtro de un objeto **Recordset**, use la constante **adFilterNone**. El establecimiento de la propiedad **Filter** en una cadena de longitud cero ("") tiene el mismo efecto que el uso de la constante **adFilterNone**.

## <a name="filtering-with-a-criteria-string"></a>Filtrar por una cadena de criterios

La cadena de criterios se compone de cláusulas con el formato *NombreCampo Operador valor* (por ejemplo, "LastName = 'Cervantes'"). Puede crear cláusulas compuestas concatenando cláusulas individuales con AND (por ejemplo, "LastName = 'Smith' AND FirstName = 'John'") y OR (por ejemplo,). Puede crear cláusulas compuestas concatenando cláusulas individuales con AND (por ejemplo, "LastName = 'Smith' AND FirstName = 'Juan'") y o (por ejemplo, "LastName = 'Smith' OR LastName = 'Jones'"). Utilice las indicaciones siguientes para las cadenas de criterios:

  - *FieldName* debe ser un nombre de campo válido desde el **conjunto de registros**. Si el nombre de campo contiene espacios, debe ir entre corchetes.

  - *Operador* debe ser uno de los siguientes: \<, \>, \<=, \>=, \< \>, = o LIKE.

  - *Valor* es el valor con el que se va a comparar los valores de campo (por ejemplo, 'Smith', \#24/8/95\#, 12.345 o $50.00). Usar comillas simples (') con las cadenas y signos de número (\#) con las fechas. Con los números puede utilizar comas decimales, signos de dólar y notación científica. Si *operador* es LIKE, *valor* puede utilizar caracteres comodín. Sólo el asterisco (\*) y el signo de porcentaje (%) se admiten caracteres comodín y deben ser el último carácter en la cadena. *Valor* no puede ser null.
    

    > [!NOTE]
    > <P>Para incluir comillas simples (') en el filtro de <EM>valor</EM>, utilice dos comillas simples para representar una. Por ejemplo, para filtrar por <EM>o ' Malley</EM>, la cadena de criterios debe ser "col1 = ' O'' Malley'". Para incluir comillas simples al principio y al final del valor de filtro, ponga la cadena entre signos de número (#). Por ejemplo, para filtrar por <EM>'1'</EM>, la cadena de criterios debería ser "col1 = #' 1' #".</P>



No se aplica ningún orden de prioridad entre AND y OR. Las cláusulas se pueden agrupar entre paréntesis. Sin embargo, no puede agrupar cláusulas unidas por un operador OR y, a continuación, unir el grupo a otra cláusula con un operador AND, como se indica a continuación:

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

En su lugar, debería crear el filtro del siguiente modo:

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

En una cláusula LIKE, puede utilizar un comodín al principio y al final del patrón (por ejemplo LastName Like '\*mit\*') o sólo al final del patrón (por ejemplo) o sólo al final del patrón (por ejemplo LastName Like ' Smit\*').

## <a name="filtering-with-a-constant"></a>Filtrar por una constante

Las constantes siguientes están disponibles para filtrar objetos **Recordset**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>Filtra de modo que sólo se vean los registros afectados por la última llamada a <strong>Delete</strong>, <strong>Resynch</strong>, <strong>UpdateBatch</strong> o <strong>CancelBatch</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>Filtra de modo que se vean los registros que no superaron la última actualización por lotes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>Filtra de modo que se vean los registros almacenados en la memoria caché actual, es decir, los resultados de la última llamada para recuperar registros de la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>Quita el filtro actual de modo que se puedan ver todos los registros.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>Filtra de modo que se vean sólo los registros que han cambiado, pero que aún no se han enviado al servidor. Sólo se aplica al modo de actualización de proceso por lotes.</p></td>
</tr>
</tbody>
</table>


Las constantes de filtro facilitan la resolución de conflictos de registros individuales durante el modo de actualización de proceso por lotes al permitir ver, por ejemplo, sólo aquellos registros que se vieron afectados durante la última llamada al método **UpdateBatch**, como se muestra en el ejemplo siguiente:

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

## <a name="filtering-with-bookmarks"></a>Filtrar por marcadores

Por último, puede pasar una matriz Variant de marcadores a la propiedad **Filter**. El cursor resultante contendrá solo aquellos registros cuyo marcador se pasó a la propiedad. En el ejemplo de código siguiente se crea una matriz de marcadores de los registros de un **conjunto de registros** que tienen una "B" en el campo *ProductName* . A continuación, se pasa la matriz a la propiedad **Filter** y se muestra información acerca del objeto **Recordset** filtrado resultante.

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

## <a name="creating-a-clone-of-a-recordset"></a>Crear un clon de un objeto Recordset

Use el método **Clone** para crear varios objetos **Recordset** duplicados, sobre todo si desea mantener más de un registro actual en un conjunto determinado de registros. El método **Clone** es más eficaz que crear y abrir un nuevo objeto **Recordset** con la misma definición que el original.

El registro actual de un clon recién creado se establece originalmente en el primer registro. El puntero del registro actual de un objeto **Recordset** clonado no está sincronizado con el original ni viceversa. Es posible navegar independientemente en cada objeto **Recordset**.

Los cambios realizados en un objeto **Recordset** se ven en todos sus duplicados, independientemente del tipo de cursor. Sin embargo, después de ejecutar [Requery](requery-method-ado.md) en el objeto **Recordset** original, los duplicados ya no estarán sincronizados con el original.

Al cerrar el objeto **Recordset** original, no se cierran sus copias; como tampoco se cierra el original ni ninguna de las demás copias al cerrarse una copia.

Se puede clonar un objeto **Recordset** sólo si admite marcadores. Los valores de los marcadores son intercambiables; es decir, una referencia de marcador de un objeto **Recordset** hace referencia al mismo registro en todos sus clones.


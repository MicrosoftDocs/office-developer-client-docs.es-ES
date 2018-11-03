---
title: Sección de esquema (referencia de escritorio de la base de datos de Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 00a5c08784d1a57e148acbaa6f1621102d6b6712
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947759"
---
# <a name="schema-section"></a><span data-ttu-id="e6e3c-102">Sección de esquema</span><span class="sxs-lookup"><span data-stu-id="e6e3c-102">Schema section</span></span>

<span data-ttu-id="e6e3c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6e3c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="schema-section"></a><span data-ttu-id="e6e3c-104">Sección de esquema</span><span class="sxs-lookup"><span data-stu-id="e6e3c-104">Schema Section</span></span>

<span data-ttu-id="e6e3c-p101">La sección de esquema no debe faltar. Como se muestra en el ejemplo anterior, ADO escribe metadatos detallados de cada columna para conservar la semántica de los valores de los datos lo máximo posible para las actualizaciones. Sin embargo, para la carga en XML, ADO sólo requiere los nombres de las columnas y del conjunto de filas al que pertenecen. Éste es un ejemplo de un esquema mínimo:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p101">The schema section is required. As the previous example shows, ADO writes out detailed metadata about each column to preserve the semantics of the data values as much as possible for updating. However, to load in the XML, ADO only requires the names of the columns and the rowset to which they belong. Here is an example of a minimal schema:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882" 
    xmlns:rs="urn:schemas-microsoft-com:rowset" 
    xmlns:z="#RowsetSchema"> 
  <s:Schema id="RowsetSchema"> 
    <s:ElementType name="row" content="eltOnly"> 
      <s:AttributeType name="ShipperID"/> 
      <s:AttributeType name="CompanyName"/> 
      <s:AttributeType name="Phone"/> 
      <s:Extends type="rs:rowbase"/> 
    </s:ElementType> 
  </s:Schema> 
  <rs:data> 
... 
  </rs:data> 
</xml> 
```

<span data-ttu-id="e6e3c-109">En el caso anterior, ADO tratará los datos como cadenas de longitud variable, ya que no se incluye ninguna información de tipos en el esquema.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-109">In the case above, ADO will treat the data as variable length strings because no type information is included in the schema.</span></span>

## <a name="creating-aliases-for-column-names"></a><span data-ttu-id="e6e3c-110">Crear alias para nombres de columnas</span><span class="sxs-lookup"><span data-stu-id="e6e3c-110">Creating Aliases for Column Names</span></span>

<span data-ttu-id="e6e3c-p102">El atributo **rs:name** permite crear un alias para un nombre de columna, de modo que aparezca un nombre descriptivo en la información de la columna expuesta por el conjunto de filas y se pueda usar un nombre más corto en la sección de datos. Por ejemplo, el esquema anterior se podría modificar para asignar ShipperID a s1, CompanyName a s2 y Phone a s3 del siguiente modo:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p102">The **rs:name** attribute allows you to create an alias for a column name so that a friendly name may appear in the column information exposed by the rowset and a shorter name may be used in the data section. For example, the schema above could be modified to map ShipperID to s1, CompanyName to s2, and Phone to s3 as follows:</span></span>

```xml 
 
<s:Schema id="RowsetSchema">  
<s:ElementType name="row" content="eltOnly" rs:updatable="true">  
<s:AttributeType name="s1" rs:name="ShipperID" rs:number="1" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s2" rs:name="CompanyName" rs:number="2" ...>  
... 
</s:AttributeType>  
<s:AttributeType name="s3" rs:name="Phone" rs:number="3" ...>  
... 
</s:AttributeType>  
... 
</s:ElementType>  
</s:Schema>  
```

<span data-ttu-id="e6e3c-113">A continuación, en la sección de datos, la fila utilizaría el atributo **name** (no **rs:name**) para hacer referencia a dicha columna:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-113">Then, in the data section, the row would use the **name** attribute (not **rs:name**) to refer to that column:</span></span>

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

<span data-ttu-id="e6e3c-p103">La creación de alias para nombres de columnas es necesaria siempre que un nombre de columna no sea un nombre de etiqueta ni un atributo legal en XML. Por ejemplo, "Last Name" (Apellidos) debe tener un alias porque los nombres con espacios intermedios no son atributos legales. El analizador de XML no procesará correctamente la siguiente línea, por lo que debe crear un alias en algún otro nombre que no contenga espacios internos:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p103">Creating aliases for column names is required whenever a column name is not a legal attribute or tag name in XML. For example, "Last Name" must have an alias because names with embedded spaces are illegal attributes. The following line won't be correctly handled by the XML parser, so you must create an alias to some other name that does not have an embedded space:</span></span>

```xml 
 
<row last name="Jones"/> 
```

<span data-ttu-id="e6e3c-p104">Cualquier valor que utilice para el atributo **name** se debe utilizar de la misma forma en cada lugar de las secciones de esquema y de datos del documento XML donde se haga referencia a la columna. En el siguiente ejemplo, se muestra el uso coherente de s1:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p104">Whatever value you use for the **name** attribute must be used consistently in each place that the column is referenced in both the schema and data sections of the XML document. The following example shows the consistent use of s1:</span></span>

```xml 
 
<s:Schema id="RowsetSchema"> 
  <s:ElementType name="row" content="eltOnly"> 
    <s:attribute type="s1"/> 
    <s:attribute type="CompanyName"/> 
    <s:attribute type="s3"/> 
    <s:extends type="rs:rowbase"/> 
  </s:ElementType> 
  <s:AttributeType name="s1" rs:name="ShipperID" rs:number="1"  
    rs:maydefer="true" rs:writeunknown="true"> 
    <s:datatype dt:type="i4" dt:maxLength="4" rs:precision="10"  
      rs:fixedlength="true" rs:maybenull="true"/> 
  </s:AttributeType> 
</s:Schema> 
<rs:data> 
  <z:row s1="1" CompanyName="Speedy Express" s3="(503) 555-9831"/> 
</rs:data> 
```

<span data-ttu-id="e6e3c-119">De igual forma, puesto que no se ha definido ningún alias para CompanyName, se debe utilizar este nombre de la misma forma en todo el documento.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-119">Similarly, because there is no alias defined for CompanyName above, CompanyName must be used consistently throughout the document.</span></span>

## <a name="data-types"></a><span data-ttu-id="e6e3c-120">Tipos de datos</span><span class="sxs-lookup"><span data-stu-id="e6e3c-120">Data Types</span></span>

<span data-ttu-id="e6e3c-p105">Puede aplicar un tipo de datos a una columna con el atributo **dt:type**. Puede especificar un tipo de datos de dos formas: especificando el atributo **dt:type** directamente en la propia definición de columna o utilizando la construcción **s:datatype** como elemento anidado de la definición de columna. Por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p105">You can apply a data type to a column with the **dt:type** attribute. You can specify a data type in two ways: either specify the **dt:type** attribute directly on the column definition itself or use the **s:datatype** construct as a nested element of the column definition. For example,</span></span>

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

<span data-ttu-id="e6e3c-124">es equivalente a</span><span class="sxs-lookup"><span data-stu-id="e6e3c-124">is equivalent to</span></span>

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

<span data-ttu-id="e6e3c-125">Si omite el atributo **dt:type** completamente de la definición de fila, el tipo de la columna será una cadena de longitud variable, de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-125">If you omit the **dt:type** attribute entirely from the row definition, by default, the column's type will be a variable length string.</span></span>

<span data-ttu-id="e6e3c-p106">Si dispone de más información de tipos que simplemente el nombre del tipo (por ejemplo, **dt:maxLength**), es más legible utilizar el elemento secundario de \*\* s:datatype\*\*. Sin embargo, se trata simplemente de una convención, no de un requisito.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p106">If you have more type information than simply the type name (for example, **dt:maxLength**), it makes it more readable to use the **s:datatype** child element. This is merely a convention, however, and not a requirement.</span></span>

<span data-ttu-id="e6e3c-128">En los ejemplos siguientes, se muestra con más detalle cómo incluir información de tipos en el esquema:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-128">The following examples show further how to include type information in your schema:</span></span>

```xml 
 
<!-- 1. String with no max length --> 
<s:AttributeType name="title_id"/> 
<! — or --> 
<s:AttributeType name="title_id" dt:type="string"/> 
 
<! — 2. Fixed length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" rs:fixedlength="true" /> 
</s:AttributeType> 
 
<! — 3. Variable length string with max length of 6 --> 
<s:AttributeType name="title_id"> 
    <s:datatype dt:type="string" dt:maxLength="6" /> 
</s:AttributeType> 
 
<! — 4. Integer --> 
<s:AttributeType name="title_id" dt:type="int"/> 
```

<span data-ttu-id="e6e3c-129">El segundo ejemplo muestra un uso sutil del atributo **rs:fixedlength**.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-129">There is a subtle use of the **rs:fixedlength** attribute in the second example.</span></span> <span data-ttu-id="e6e3c-130">Una columna cuyo atributo **rs:fixedlength** se establece en el valor true (verdadero) significa que los datos deben tener la longitud definida en el esquema.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-130">A column with the **rs:fixedlength** attribute set to true means that the data must have the length defined in the schema.</span></span> <span data-ttu-id="e6e3c-131">En este caso, el valor de un departamento jurídico para título\_identificador es "123456", tal como está "123".</span><span class="sxs-lookup"><span data-stu-id="e6e3c-131">In this case, a legal value for title\_id is "123456," as is "123 ."</span></span> <span data-ttu-id="e6e3c-132">Sin embargo, "123" no sería válido, ya que su longitud es 3, no 6.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-132">However, "123" would not be valid because its length is 3, not 6.</span></span> <span data-ttu-id="e6e3c-133">Vea la Guía del programador de OLE DB para obtener una descripción más completa de la propiedad **fixedlength**.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-133">See the OLE DB Programmer's Guide for a more complete description of the **fixedlength** property.</span></span>

## <a name="handling-nulls"></a><span data-ttu-id="e6e3c-134">Tratamiento de valores nulos</span><span class="sxs-lookup"><span data-stu-id="e6e3c-134">Handling Nulls</span></span>

<span data-ttu-id="e6e3c-p108">Los valores nulos (null) los controla el atributo **rs:maybenull**. Si se establece el valor de este atributo en true (verdadero), el contenido de la columna puede ser un valor nulo. Además, si la columna no se encuentra en una fila de datos, el usuario que lee los datos de nuevo del conjunto de filas obtendrá un estado nulo desde **IRowset::GetData()**. Considere las definiciones siguientes de columna de la tabla Shippers:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-p108">Null values are handled by the **rs:maybenull** attribute. If this attribute is set to true, the contents of the column may contain a null value. Furthermore, if the column is not found in a row of data, the user reading the data back from the rowset will get a null status from **IRowset::GetData()**. Consider the following column definitions from the Shippers table:</span></span>

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

<span data-ttu-id="e6e3c-139">La definición permite que CompanyName sea nulo, pero ShipperID no puede contener ningún valor nulo.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-139">The definition allows CompanyName to be null, but ShipperID cannot contain a null value.</span></span> <span data-ttu-id="e6e3c-140">Si la sección de datos contenía la fila siguiente, el proveedor de persistencia establecería el estado de los datos para la columna CompanyName a la constante de estado de OLE DB DBSTATUS\_S\_ISNULL:</span><span class="sxs-lookup"><span data-stu-id="e6e3c-140">If the data section contained the following row, the Persistence Provider would set the status of the data for the CompanyName column to the OLE DB status constant DBSTATUS\_S\_ISNULL:</span></span>

```xml 
 
<z:row ShipperID="1"/> 
```

<span data-ttu-id="e6e3c-141">Si la fila estaba totalmente vacía, como se indica a continuación, el proveedor de persistencia devolvería un estado OLE DB de DBSTATUS\_E\_no disponible para ShipperID y DBSTATUS\_S\_ISNULL para CompanyName.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-141">If the row was entirely empty, as follows, the Persistence Provider would return an OLE DB status of DBSTATUS\_E\_UNAVAILABLE for ShipperID and DBSTATUS\_S\_ISNULL for CompanyName.</span></span>

```xml 
 
<z:row/>  
```

<span data-ttu-id="e6e3c-142">Tenga en cuenta que una cadena de longitud cero no es lo mismo que un valor null.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-142">Note that a zero-length string is not the same as null.</span></span>

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

<span data-ttu-id="e6e3c-143">Para la fila anterior, el proveedor de persistencia devolverá un estado OLE DB de DBSTATUS\_S\_Aceptar para ambas columnas.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-143">For the preceding row, the Persistence Provider will return an OLE DB status of DBSTATUS\_S\_OK for both columns.</span></span> <span data-ttu-id="e6e3c-144">En este caso, CompanyName es simplemente "" (una cadena de longitud cero).</span><span class="sxs-lookup"><span data-stu-id="e6e3c-144">The CompanyName in this case is simply "" (a zero-length string).</span></span>

<span data-ttu-id="e6e3c-145">Para obtener más información acerca de las construcciones OLE DB disponibles para su uso en el esquema de un documento XML para OLE DB, vea la definición de "urn:schemas-microsoft-com:rowset" y la Guía del programador de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e6e3c-145">For further information about the OLE DB constructs available for use within the schema of an XML document for OLE DB, see the definition of "urn:schemas-microsoft-com:rowset" and the OLE DB Programmer's Guide.</span></span>


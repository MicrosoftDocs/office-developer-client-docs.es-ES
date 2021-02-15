---
title: Sección Esquema (referencia de base de datos de escritorio de Access)
TOCTitle: Schema Section
ms:assetid: 59b42ffb-0524-adc3-8bcd-6e4cd2c505ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249304(v=office.15)
ms:contentKeyID: 48545023
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8c479c430dd6d0ca742fefb4948544d31ba2e61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308942"
---
# <a name="schema-section"></a>Sección de esquema

**Se aplica a:** Access 2013, Office 2013

## <a name="schema-section"></a>Sección de esquema

La sección de esquema no debe faltar. Como se muestra en el ejemplo anterior, ADO escribe metadatos detallados de cada columna para conservar la semántica de los valores de los datos lo máximo posible para las actualizaciones. Sin embargo, para la carga en XML, ADO sólo requiere los nombres de las columnas y del conjunto de filas al que pertenecen. Éste es un ejemplo de un esquema mínimo:

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

En el caso anterior, ADO tratará los datos como cadenas de longitud variable, ya que no se incluye ninguna información de tipos en el esquema.

## <a name="creating-aliases-for-column-names"></a>Crear alias para nombres de columnas

El atributo **rs:name** permite crear un alias para un nombre de columna, de modo que aparezca un nombre descriptivo en la información de la columna expuesta por el conjunto de filas y se pueda usar un nombre más corto en la sección de datos. Por ejemplo, el esquema anterior se podría modificar para asignar ShipperID a s1, CompanyName a s2 y Phone a s3 del siguiente modo:

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

A continuación, en la sección de datos, la fila utilizaría el atributo **name** (no **rs:name**) para hacer referencia a dicha columna:

```xml 
 
"<row s1="1" s2="Speedy Express" s3="(503) 555-9831"/> 
```

La creación de alias para nombres de columnas es necesaria siempre que un nombre de columna no sea un nombre de etiqueta ni un atributo legal en XML. Por ejemplo, "Last Name" (Apellidos) debe tener un alias porque los nombres con espacios intermedios no son atributos legales. El analizador de XML no procesará correctamente la siguiente línea, por lo que debe crear un alias en algún otro nombre que no contenga espacios internos:

```xml 
 
<row last name="Jones"/> 
```

Cualquier valor que utilice para el atributo **name** se debe utilizar de la misma forma en cada lugar de las secciones de esquema y de datos del documento XML donde se haga referencia a la columna. En el siguiente ejemplo, se muestra el uso coherente de s1:

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

De igual forma, puesto que no se ha definido ningún alias para CompanyName, se debe utilizar este nombre de la misma forma en todo el documento.

## <a name="data-types"></a>Tipos de datos

Puede aplicar un tipo de datos a una columna con el atributo **dt:type**. Puede especificar un tipo de datos de dos formas: especificando el atributo **dt:type** directamente en la propia definición de columna o utilizando la construcción **s:datatype** como elemento anidado de la definición de columna. Por ejemplo,

```xml 
 
<s:AttributeType name="Phone" > 
  <s:datatype dt:type="string"/> 
</s:AttributeType> 
```

es equivalente a

```xml 
 
<s:AttributeType name="Phone" dt:type="string"/> 
```

Si omite el atributo **dt:type** completamente de la definición de fila, el tipo de la columna será una cadena de longitud variable, de forma predeterminada.

Si dispone de más información de tipos que simplemente el nombre del tipo (por ejemplo, **dt:maxLength**), es más legible utilizar el elemento secundario de **s:datatype**. Sin embargo, se trata simplemente de una convención, no de un requisito.

En los ejemplos siguientes, se muestra con más detalle cómo incluir información de tipos en el esquema:

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

El segundo ejemplo muestra un uso sutil del atributo **rs:fixedlength**. Una columna cuyo atributo **rs:fixedlength** se establece en el valor true (verdadero) significa que los datos deben tener la longitud definida en el esquema. En este caso, un valor legal para el identificador de título es \_ "123456", al igual que "123 ". Sin embargo, "123" no sería válido, ya que su longitud es 3, no 6. Vea la Guía del programador de OLE DB para obtener una descripción más completa de la propiedad **fixedlength**.

## <a name="handling-nulls"></a>Tratamiento de valores nulos

Los valores nulos (null) los controla el atributo **rs:maybenull**. Si se establece el valor de este atributo en true (verdadero), el contenido de la columna puede ser un valor nulo. Además, si la columna no se encuentra en una fila de datos, el usuario que lee los datos de nuevo del conjunto de filas obtendrá un estado nulo desde **IRowset::GetData()**. Considere las definiciones siguientes de columna de la tabla Shippers:

```xml 
 
<s:AttributeType name="ShipperID"> 
  <s:datatype dt:type="int" dt:maxLength="4"/> 
</s:AttributeType> 
<s:AttributeType name="CompanyName"> 
  <s:datatype dt:type="string" dt:maxLength="40" rs:maybenull="true"/> 
</s:AttributeType> 
```

La definición permite que CompanyName sea nulo, pero ShipperID no puede contener ningún valor nulo. Si la sección de datos contenía la siguiente fila, el proveedor de persistencia establecería el estado de los datos de la columna CompanyName en la constante de estado DBSTATUS S ISNULL de OLE \_ \_ DB:

```xml 
 
<z:row ShipperID="1"/> 
```

Si la fila estaba completamente vacía, como se muestra a continuación, el proveedor de persistencia devolvería un estado OLE DBSTATUS E UNAVAILABLE para \_ \_ ShipperID y DBSTATUS \_ S \_ ISNULL para CompanyName.

```xml 
 
<z:row/>  
```

Tenga en cuenta que una cadena de longitud cero no es lo mismo que un valor null.

```xml 
 
<z:row ShipperID="1" CompanyName=""/> 
```

Para la fila anterior, el proveedor de persistencia devolverá un estado OLE DB de DBSTATUS \_ S OK para ambas \_ columnas. En este caso, CompanyName es simplemente "" (una cadena de longitud cero).

Para obtener más información acerca de las construcciones OLE DB disponibles para su uso en el esquema de un documento XML para OLE DB, vea la definición de "urn:schemas-microsoft-com:rowset" y la Guía del programador de OLE DB.


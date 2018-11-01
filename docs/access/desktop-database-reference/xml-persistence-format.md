---
title: Formato de persistencia XML
TOCTitle: XML Persistence Format
ms:assetid: 499f335c-ee1f-c803-e3a8-034b8decf1ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249226(v=office.15)
ms:contentKeyID: 48544643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 201ea2b46ad2bb08e631882cebd5419b6b301179
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867751"
---
# <a name="xml-persistence-format"></a><span data-ttu-id="631fb-102">Formato de persistencia XML</span><span class="sxs-lookup"><span data-stu-id="631fb-102">XML Persistence Format</span></span>

<span data-ttu-id="631fb-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="631fb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="631fb-104">Formato de persistencia XML</span><span class="sxs-lookup"><span data-stu-id="631fb-104">XML Persistence Format</span></span>

<span data-ttu-id="631fb-105">ADO utiliza la codificación UTF-8 para la secuencia XML que almacena.</span><span class="sxs-lookup"><span data-stu-id="631fb-105">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="631fb-p101">El formato XML de ADO se divide en dos secciones, una sección de esquema seguida de otra de datos. A continuación, se proporciona un ejemplo de archivo XML para la tabla Shippers de la base de datos Neptuno. Después del ejemplo, se analizan diversas partes del XML.</span><span class="sxs-lookup"><span data-stu-id="631fb-p101">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="631fb-p102">El esquema muestra las declaraciones de espacio de nombres, las secciones de esquema y de datos. La sección de esquema contiene definiciones para fila, ShipperID, CompanyName y Phone.</span><span class="sxs-lookup"><span data-stu-id="631fb-p102">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="631fb-p103">Las definiciones de esquema cumplen la especificación XML-Data y se pueden validar totalmente (aunque la validación no funcionará en Internet Explorer 5). Puede ver esta especificación en [Notas sobre W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data es actualmente el único formato de esquema admitido para persistencia de **conjuntos de registros**.</span><span class="sxs-lookup"><span data-stu-id="631fb-p103">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="631fb-114">La sección de datos tiene tres filas que contienen información sobre compañías de envío.</span><span class="sxs-lookup"><span data-stu-id="631fb-114">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="631fb-115">Para un conjunto de filas vacío, la sección de datos puede estar vacía, pero la `<rs:data>` etiquetas deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="631fb-115">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="631fb-116">Sin datos, podría escribir la etiqueta de forma abreviada como simplemente `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="631fb-116">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="631fb-117">Cualquier etiqueta con el prefijo "rs" indica que se encuentra en el espacio de nombres definido por urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="631fb-117">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="631fb-118">La definición completa de este esquema se muestra en el apéndice de este documento.</span><span class="sxs-lookup"><span data-stu-id="631fb-118">The full definition of this schema is defined in the appendix to this document.</span></span>

## <a name="xml-persistence-format"></a><span data-ttu-id="631fb-119">Formato de persistencia XML</span><span class="sxs-lookup"><span data-stu-id="631fb-119">XML Persistence Format</span></span>

<span data-ttu-id="631fb-120">ADO utiliza la codificación UTF-8 para la secuencia XML que almacena.</span><span class="sxs-lookup"><span data-stu-id="631fb-120">ADO uses UTF-8 encoding for the XML stream it persists.</span></span>

<span data-ttu-id="631fb-p105">El formato XML de ADO se divide en dos secciones, una sección de esquema seguida de otra de datos. A continuación, se proporciona un ejemplo de archivo XML para la tabla Shippers de la base de datos Neptuno. Después del ejemplo, se analizan diversas partes del XML.</span><span class="sxs-lookup"><span data-stu-id="631fb-p105">The ADO XML format is broken into two sections, a schema section followed by the data section. The following is an example XML file for the Shippers table from the Northwind database. Various parts of the XML are discussed following the example.</span></span>

```xml
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"  
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"  
xmlns:rs="urn:schemas-microsoft-com:rowset"  
xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="ShipperID" rs:number="1"  
        rs:basetable="shippers" rs:basecolumn="ShipperID" 
        rs:keycolumn="true">  
        <s:datatype dt:type="int" dt:maxLength="4" rs:precision="10"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="CompanyName" rs:number="2"  
        rs:nullable="true" rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="CompanyName">  
        <s:datatype dt:type="string" dt:maxLength="40" />  
      </s:AttributeType>  
      <s:AttributeType name="Phone" rs:number="3" rs:nullable="true"  
        rs:write="true" rs:basetable="shippers"  
        rs:basecolumn="Phone">  
        <s:datatype dt:type="string" dt:maxLength="24"/>  
      </s:AttributeType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
 
  <rs:data>  
    <z:row ShipperID="1" CompanyName="Speedy Express"  
      Phone="(503) 555-9831"/>  
    <z:row ShipperID="2" CompanyName="United Package"  
      Phone="(503) 555-3199"/>  
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/>  
  </rs:data>  
</xml> 
```

<span data-ttu-id="631fb-p106">El esquema muestra las declaraciones de espacio de nombres, las secciones de esquema y de datos. La sección de esquema contiene definiciones para fila, ShipperID, CompanyName y Phone.</span><span class="sxs-lookup"><span data-stu-id="631fb-p106">The schema shows the declarations of namespaces, the schema section, and the data section. The schema section contains definitions for row, ShipperID, CompanyName, and Phone.</span></span>

<span data-ttu-id="631fb-p107">Las definiciones de esquema cumplen la especificación XML-Data y se pueden validar totalmente (aunque la validación no funcionará en Internet Explorer 5). Puede ver esta especificación en [Notas sobre W3C XMLData](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data es actualmente el único formato de esquema admitido para persistencia de **conjuntos de registros**.</span><span class="sxs-lookup"><span data-stu-id="631fb-p107">Schema definitions conform to the XML-Data specification and are able to be fully validated (though validation will not occur in Internet Explorer 5). You can view this specification at [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/). XML-Data is the only supported schema format for **Recordset** persistence currently.</span></span>

<span data-ttu-id="631fb-129">La sección de datos tiene tres filas que contienen información sobre compañías de envío.</span><span class="sxs-lookup"><span data-stu-id="631fb-129">The data section has three rows containing information about shippers.</span></span> <span data-ttu-id="631fb-130">Para un conjunto de filas vacío, la sección de datos puede estar vacía, pero la `<rs:data>` etiquetas deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="631fb-130">For an empty rowset, the data section may be empty, but the `<rs:data>` tags must be present.</span></span> <span data-ttu-id="631fb-131">Sin datos, podría escribir la etiqueta de forma abreviada como simplemente `<rs:data>`.</span><span class="sxs-lookup"><span data-stu-id="631fb-131">With no data, you could write the tag shorthand as simply `<rs:data>`.</span></span> <span data-ttu-id="631fb-132">Cualquier etiqueta con el prefijo "rs" indica que se encuentra en el espacio de nombres definido por urn:schemas-microsoft-com:rowset.</span><span class="sxs-lookup"><span data-stu-id="631fb-132">Any tag prefixed with "rs" indicates that it is in the namespace defined by urn:schemas-microsoft-com:rowset.</span></span> <span data-ttu-id="631fb-133">La definición completa de este esquema se muestra en el apéndice de este documento.</span><span class="sxs-lookup"><span data-stu-id="631fb-133">The full definition of this schema is defined in the appendix to this document.</span></span>


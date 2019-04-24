---
title: Sección de datos (referencia de base de datos de escritorio de Access)
TOCTitle: Data section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b8e3baf4d147edcc739e59933da4697c08cdef0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295047"
---
# <a name="data-section"></a><span data-ttu-id="daf89-102">Sección de datos</span><span class="sxs-lookup"><span data-stu-id="daf89-102">Data section</span></span>

<span data-ttu-id="daf89-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daf89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daf89-p101">La sección de datos define los datos del conjunto de filas junto con el resto de actualizaciones, inserciones o eliminaciones pendientes. La sección de datos puede contener cero o varias filas. Puede contener únicamente datos de un conjunto de filas en el que la fila está definida por el esquema. Además, como se indicó previamente, se pueden omitir las columnas que no contengan datos. Si se utiliza un atributo o un subelemento en la sección de datos y este diseño no se ha definido en la sección de esquema, se omite silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="daf89-p101">The data section defines the data of the rowset along with any pending updates, insertions, or deletions. The data section may contain zero or more rows. It may only contain data from one rowset where the row is defined by the schema. Also, as noted before, columns without any data may be omitted. If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="daf89-109">String</span><span class="sxs-lookup"><span data-stu-id="daf89-109">String</span></span>

<span data-ttu-id="daf89-p102">Los caracteres reservados en XML incluidos en datos de texto se deben reemplazar por entidades de carácter apropiadas. Por ejemplo, en el nombre de empresa "Joe's Garage", el carácter de comilla simple se debe reemplazar por una entidad. La fila real tendría este aspecto:</span><span class="sxs-lookup"><span data-stu-id="daf89-p102">Reserved XML characters in text data must be replaced with appropriate character entities. For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity. The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="daf89-113">Los siguientes caracteres están reservados en XML y se deben reemplazar por entidades de carácter: {', ", &\<,\>,}.</span><span class="sxs-lookup"><span data-stu-id="daf89-113">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="daf89-114">Binary</span><span class="sxs-lookup"><span data-stu-id="daf89-114">Binary</span></span>

<span data-ttu-id="daf89-115">Los datos binarios tienen codificación bin.hex (es decir, un byte se asigna a dos caracteres, un carácter por cada medio byte).</span><span class="sxs-lookup"><span data-stu-id="daf89-115">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="daf89-116">DateTime</span><span class="sxs-lookup"><span data-stu-id="daf89-116">DateTime</span></span>

<span data-ttu-id="daf89-117">Los tipos de\_datos de datos XML no admiten directamente el formato de fecha Variant VT.</span><span class="sxs-lookup"><span data-stu-id="daf89-117">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="daf89-118">El formato correcto para las fechas con componente de fecha y de hora es aaaa-mm-dd**T**hh:mm:ss.</span><span class="sxs-lookup"><span data-stu-id="daf89-118">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="daf89-119">Para obtener más información acerca de los formatos de fecha especificados por XML, vea la [Nota de XMLData de W3C](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="daf89-119">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="daf89-120">Cuando la especificación de datos XML define dos tipos de datos equivalentes (por ejemplo, i4 == int), ADO escribe el nombre descriptivo pero lee ambos.</span><span class="sxs-lookup"><span data-stu-id="daf89-120">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="daf89-121">Administración de los cambios pendientes</span><span class="sxs-lookup"><span data-stu-id="daf89-121">Managing pending changes</span></span>

<span data-ttu-id="daf89-p104">Un **conjunto de registros** se puede abrir en modo de actualización inmediata o por lotes. Si se abre en modo de actualización por lotes con cursores de cliente, todos los cambios realizados en el **conjunto de registros** quedan en estado pendiente hasta que se llame al método **UpdateBatch**. Los cambios pendientes también se conservan cuando se guarda el **conjunto de registros**. En XML, se representan mediante el uso de los elementos de "actualización" definidos en urn:schemas-microsoft-com:rowset. Además, si un conjunto de filas se puede actualizar, la propiedad actualizable debe establecerse en True en la definición de la fila. Por ejemplo, para definir que la tabla Transportistas (Shippers) contiene cambios pendientes, la definición de fila debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="daf89-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="daf89-128">Así, se indica al proveedor de persistencia que muestre datos para que ADO pueda diseñar un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="daf89-128">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="daf89-129">Los datos de ejemplo siguientes muestran el aspecto de inserciones, cambios y eliminaciones en el archivo conservado:</span><span class="sxs-lookup"><span data-stu-id="daf89-129">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

```xml 
<rs:data> 
  <z:row ShipperID="2" CompanyName="United Package"  
    Phone="(503) 555-3199"/> 
<rs:update> 
  <rs:original> 
    <z:row ShipperID="3" CompanyName="Federal Shipping"  
      Phone="(503) 555-9931"/> 
  </rs:original> 
  <z:row Phone="(503) 552-7134"/> 
</rs:update> 
<rs:insert> 
  <z:row ShipperID="12" CompanyName="Lightning Shipping"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="13" CompanyName="Thunder Overnight"  
    Phone="(505) 111-2222"/> 
  <z:row ShipperID="14" CompanyName="Blue Angel Air Delivery"  
    Phone="(505) 111-2222"/> 
</rs:insert> 
<rs:delete> 
  <z:row ShipperID="1" CompanyName="Speedy Express" Phone="(503) 555-9831"/> 
</rs:delete> 
</rs:data> 
```

<span data-ttu-id="daf89-p105">Una actualización siempre contiene todos los datos originales de la fila seguidos de los datos cambiados de la fila. La fila modificada puede contener todas las columnas o sólo aquellas columnas que se hayan cambiado realmente. En el ejemplo anterior, la fila correspondiente a Transportista 2 (Shipper 2) no ha cambiado, mientras que en la columna Teléfono (Phone) sólo ha cambiado el valor para Transportista 3 (Shipper 3) y, por lo tanto, es la única columna incluida en la fila modificada. Las filas insertadas para los transportistas 12, 13 y 14 se agrupan en un lote con una etiqueta rs:insert. Tenga en cuenta que también se pueden agrupar en un lote las filas eliminadas, aunque esto no se muestra en el ejemplo precedente.</span><span class="sxs-lookup"><span data-stu-id="daf89-p105">An update always contains the entire original row data followed by the changed row data. The changed row may contain all of the columns or only those columns that have actually changed. In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row. The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag. Note that deleted rows may also be batched together, although this is not shown above.</span></span>


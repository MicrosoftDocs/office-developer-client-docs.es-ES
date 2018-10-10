---
title: Sección de datos (referencia de escritorio de la base de datos de Access)
TOCTitle: Data Section
ms:assetid: fd8d31aa-af13-a52f-5e91-20225b8df175
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250303(v=office.15)
ms:contentKeyID: 48548920
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19ce858f46177b603fcd6e63f55b4ed7e424deb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485706"
---
# <a name="data-section"></a><span data-ttu-id="714a5-102">Sección de datos</span><span class="sxs-lookup"><span data-stu-id="714a5-102">Data Section</span></span>

<span data-ttu-id="714a5-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="714a5-103">**Applies to**: Access 2013 | Office 2013</span></span>
 
## <a name="data-section"></a><span data-ttu-id="714a5-104">Sección de datos</span><span class="sxs-lookup"><span data-stu-id="714a5-104">Data Section</span></span>

<span data-ttu-id="714a5-p101">La sección de datos define los datos del conjunto de filas junto con el resto de actualizaciones, inserciones o eliminaciones pendientes. La sección de datos puede contener cero o varias filas. Puede contener únicamente datos de un conjunto de filas en el que la fila está definida por el esquema. Además, como se indicó previamente, se pueden omitir las columnas que no contengan datos. Si se utiliza un atributo o un subelemento en la sección de datos y este diseño no se ha definido en la sección de esquema, se omite silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="714a5-p101">The data section defines the data of the rowset along with any pending updates, insertions, or deletions. The data section may contain zero or more rows. It may only contain data from one rowset where the row is defined by the schema. Also, as noted before, columns without any data may be omitted. If an attribute or subelement is used in the data section and that construct has not been defined in the schema section, it is silently ignored.</span></span>

## <a name="string"></a><span data-ttu-id="714a5-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="714a5-110">String</span></span>

<span data-ttu-id="714a5-p102">Los caracteres reservados en XML incluidos en datos de texto se deben reemplazar por entidades de carácter apropiadas. Por ejemplo, en el nombre de empresa "Joe's Garage", el carácter de comilla simple se debe reemplazar por una entidad. La fila real tendría este aspecto:</span><span class="sxs-lookup"><span data-stu-id="714a5-p102">Reserved XML characters in text data must be replaced with appropriate character entities. For example, in the company name "Joe's Garage," the single quote character must be replaced by an entity. The actual row would look like:</span></span>

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

<span data-ttu-id="714a5-114">Los siguientes caracteres están reservados en XML y se deben reemplazar por entidades de carácter: {', "&,\<,\>}.</span><span class="sxs-lookup"><span data-stu-id="714a5-114">The following characters are reserved in XML and must be replaced by character entities: {',",&,\<,\>}.</span></span>

## <a name="binary"></a><span data-ttu-id="714a5-115">Binario</span><span class="sxs-lookup"><span data-stu-id="714a5-115">Binary</span></span>

<span data-ttu-id="714a5-116">Los datos binarios tienen codificación bin.hex (es decir, un byte se asigna a dos caracteres, un carácter por cada medio byte).</span><span class="sxs-lookup"><span data-stu-id="714a5-116">Binary data is bin.hex encoded (that is, one byte maps to two characters, one character per nibble).</span></span>

## <a name="datetime"></a><span data-ttu-id="714a5-117">DateTime</span><span class="sxs-lookup"><span data-stu-id="714a5-117">DateTime</span></span>

<span data-ttu-id="714a5-118">El valor de variant VT\_formato de fecha no es compatible directamente con tipos de datos de datos XML.</span><span class="sxs-lookup"><span data-stu-id="714a5-118">The variant VT\_DATE format is not directly supported by XML-Data data types.</span></span> <span data-ttu-id="714a5-119">El formato correcto para las fechas con componente de fecha y de hora es aaaa-mm-dd**T**ss.</span><span class="sxs-lookup"><span data-stu-id="714a5-119">The correct format for dates with both a data and time component is yyyy-mm-dd**T**hh:mm:ss.</span></span>

<span data-ttu-id="714a5-120">Para obtener más información acerca de los formatos de fecha especificados mediante XML, consulte la [Nota de la nota de W3C](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span><span class="sxs-lookup"><span data-stu-id="714a5-120">For more information about date formats specified by XML, see [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).</span></span>

<span data-ttu-id="714a5-121">Cuando la especificación de datos XML define dos tipos de datos equivalentes (por ejemplo, i4 == int), ADO escribe el nombre descriptivo pero lee ambos.</span><span class="sxs-lookup"><span data-stu-id="714a5-121">When the XML-Data specification defines two equivalent data types (for example, i4 == int), ADO will write out the friendly name but read in both.</span></span>

## <a name="managing-pending-changes"></a><span data-ttu-id="714a5-122">Administrar cambios pendientes</span><span class="sxs-lookup"><span data-stu-id="714a5-122">Managing Pending Changes</span></span>

<span data-ttu-id="714a5-p104">Un **conjunto de registros** se puede abrir en modo de actualización inmediata o por lotes. Si se abre en modo de actualización por lotes con cursores de cliente, todos los cambios realizados en el **conjunto de registros** quedan en estado pendiente hasta que se llame al método **UpdateBatch**. Los cambios pendientes también se conservan cuando se guarda el **conjunto de registros**. En XML, se representan mediante el uso de los elementos de "actualización" definidos en urn:schemas-microsoft-com:rowset. Además, si un conjunto de filas se puede actualizar, la propiedad actualizable debe establecerse en True en la definición de la fila. Por ejemplo, para definir que la tabla Transportistas (Shippers) contiene cambios pendientes, la definición de fila debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="714a5-p104">A **Recordset** can be opened in immediate or batch update mode. When opened in batch update mode with client-side cursors, all changes made to the **Recordset** are in a pending state until the **UpdateBatch** method is called. Pending changes are also persisted when the **Recordset** is saved. In XML, they are represented by the use of the "update" elements defined in urn:schemas-microsoft-com:rowset. In addition, if a rowset can be updated, the updatable property must be set to true in the definition of the row. For example, to define that the Shippers table contains pending changes, the row definition would look like the following:</span></span>

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

<span data-ttu-id="714a5-129">Así, se indica al proveedor de persistencia que muestre datos para que ADO pueda diseñar un objeto **Recordset** actualizable.</span><span class="sxs-lookup"><span data-stu-id="714a5-129">This tells the Persistence Provider to surface data so that ADO can construct an updatable **Recordset** object.</span></span>

<span data-ttu-id="714a5-130">Los datos de ejemplo siguientes muestran el aspecto de inserciones, cambios y eliminaciones en el archivo conservado:</span><span class="sxs-lookup"><span data-stu-id="714a5-130">The following sample data shows how insertions, changes, and deletions look in the persisted file:</span></span>

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

<span data-ttu-id="714a5-p105">Una actualización siempre contiene todos los datos originales de la fila seguidos de los datos cambiados de la fila. La fila modificada puede contener todas las columnas o sólo aquellas columnas que se hayan cambiado realmente. En el ejemplo anterior, la fila correspondiente a Transportista 2 (Shipper 2) no ha cambiado, mientras que en la columna Teléfono (Phone) sólo ha cambiado el valor para Transportista 3 (Shipper 3) y, por lo tanto, es la única columna incluida en la fila modificada. Las filas insertadas para los transportistas 12, 13 y 14 se agrupan en un lote con una etiqueta rs:insert. Tenga en cuenta que también se pueden agrupar en un lote las filas eliminadas, aunque esto no se muestra en el ejemplo precedente.</span><span class="sxs-lookup"><span data-stu-id="714a5-p105">An update always contains the entire original row data followed by the changed row data. The changed row may contain all of the columns or only those columns that have actually changed. In the previous example, the row for Shipper 2 is not changed, while only the Phone column has changed values for Shipper 3 and is therefore the only column included in the changed row. The inserted rows for Shippers 12, 13, and 14 are batched together under one rs:insert tag. Note that deleted rows may also be batched together, although this is not shown above.</span></span>


---
title: Sección Datos (referencia de base de datos de escritorio de Access)
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
# <a name="data-section"></a>Sección de datos

**Se aplica a:** Access 2013, Office 2013

La sección de datos define los datos del conjunto de filas junto con el resto de actualizaciones, inserciones o eliminaciones pendientes. La sección de datos puede contener cero o varias filas. Puede contener únicamente datos de un conjunto de filas en el que la fila está definida por el esquema. Además, como se indicó previamente, se pueden omitir las columnas que no contengan datos. Si se utiliza un atributo o un subelemento en la sección de datos y este diseño no se ha definido en la sección de esquema, se omite silenciosamente.

## <a name="string"></a>Cadena

Los caracteres reservados en XML incluidos en datos de texto se deben reemplazar por entidades de carácter apropiadas. Por ejemplo, en el nombre de empresa "Joe's Garage", el carácter de comilla simple se debe reemplazar por una entidad. La fila real tendría este aspecto:

```xml  
<z:row CompanyName="Joe&apos;s Garage"/> 
```

Los siguientes caracteres están reservados en XML y deben reemplazarse por entidades de caracteres: {',",&, \< , \> }.

## <a name="binary"></a>Binario

Los datos binarios tienen codificación bin.hex (es decir, un byte se asigna a dos caracteres, un carácter por cada medio byte).

## <a name="datetime"></a>DateTime

El formato DATE \_ VT variant no es compatible directamente con los XML-Data de datos. El formato correcto para las fechas con componente de fecha y de hora es aaaa-mm-dd **T** hh:mm:ss.

Para obtener más información acerca de los formatos de fecha especificados por XML, vea [W3C XMLData Note](https://www.w3.org/TR/1998/NOTE-XML-data-0105/).

Cuando la especificación de datos XML define dos tipos de datos equivalentes (por ejemplo, i4 == int), ADO escribe el nombre descriptivo pero lee ambos.

## <a name="managing-pending-changes"></a>Administración de cambios pendientes

Un **conjunto de registros** se puede abrir en modo de actualización inmediata o por lotes. Si se abre en modo de actualización por lotes con cursores de cliente, todos los cambios realizados en el **conjunto de registros** quedan en estado pendiente hasta que se llame al método **UpdateBatch**. Los cambios pendientes también se conservan cuando se guarda el **conjunto de registros**. En XML, se representan mediante el uso de los elementos de "actualización" definidos en urn:schemas-microsoft-com:rowset. Además, si un conjunto de filas se puede actualizar, la propiedad actualizable debe establecerse en True en la definición de la fila. Por ejemplo, para definir que la tabla Transportistas (Shippers) contiene cambios pendientes, la definición de fila debe tener el siguiente aspecto:

```xml 
<s:ElementType name="row" content="eltOnly" updatable="true"> 
  <s:attribute type="ShipperID"/> 
  <s:attribute type="CompanyName"/> 
  <s:attribute type="Phone"/> 
  <s:extends type="rs:rowbase"/> 
</s:ElementType> 
```

Así, se indica al proveedor de persistencia que muestre datos para que ADO pueda diseñar un objeto **Recordset** actualizable.

Los datos de ejemplo siguientes muestran el aspecto de inserciones, cambios y eliminaciones en el archivo conservado:

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

Una actualización siempre contiene todos los datos originales de la fila seguidos de los datos cambiados de la fila. La fila modificada puede contener todas las columnas o sólo aquellas columnas que se hayan cambiado realmente. En el ejemplo anterior, la fila correspondiente a Transportista 2 (Shipper 2) no ha cambiado, mientras que en la columna Teléfono (Phone) sólo ha cambiado el valor para Transportista 3 (Shipper 3) y, por lo tanto, es la única columna incluida en la fila modificada. Las filas insertadas para los transportistas 12, 13 y 14 se agrupan en un lote con una etiqueta rs:insert. Tenga en cuenta que también se pueden agrupar en un lote las filas eliminadas, aunque esto no se muestra en el ejemplo precedente.


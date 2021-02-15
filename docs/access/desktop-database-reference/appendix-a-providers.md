---
title: 'Apéndice A: Proveedores'
TOCTitle: 'Appendix A: Providers'
ms:assetid: b3f92279-8d66-ad59-71c4-c0448168125a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249857(v=office.15)
ms:contentKeyID: 48547207
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4549c8817361cfb5b9fa730ee37ca6a07edc98b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297063"
---
# <a name="appendix-a-providers"></a>Apéndice A: Proveedores


**Se aplica a:** Access 2013, Office 2013


En esta sección se habla sobre tres tipos de proveedores: proveedores de datos, de servicios y componentes de servicios. Los proveedores se clasifican en dos categorías: aquellos que proporcionan datos y aquellos que proporcionan servicios. Un *proveedor de datos* posee sus propios datos y los expone en un formato de tabla en la aplicación del usuario. Un *proveedor de servicios* encapsula un servicio al producir y consumir datos, con lo que aumentan las características de las aplicaciones ADO del usuario. Un proveedor de servicios también puede definirse como un *componente de servicios*, que debe trabajar en cooperación con otros proveedores o componentes de servicios.

## <a name="data-providers"></a>Proveedores de datos

ADO es eficaz y flexible porque puede conectar con varios proveedores de datos distintos y seguir exponiendo el mismo modelo de programación, independientemente de las características específicas de un proveedor concreto.

No obstante, dado que cada proveedor de datos es único, el modo en que la aplicación interactúa con ADO variará ligeramente según el proveedor. Las diferencias suelen clasificarse en tres categorías:

- Parámetros de conexión de la propiedad [ConnectionString](connectionstring-property-ado.md).

- Uso de objeto [Command](command-object-ado.md).

- Comportamiento del objeto [Recordset](recordset-object-ado.md) del proveedor.

A continuación puede ver los detalles de cada uno de los proveedores de datos disponibles en la actualidad desde Microsoft.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Área</p></th>
<th><p>Tema</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Bases de datos ODBC</p></td>
<td><p><a href="microsoft-ole-db-provider-for-odbc.md">Proveedor de Microsoft OLE DB para ODBC</a></p></td>
</tr>
<tr class="even">
<td><p>Servicios de Index Server de Microsoft</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-indexing-service.md">Proveedor de Microsoft OLE DB para Servicios de Index Server de Microsoft</a></p></td>
</tr>
<tr class="odd">
<td><p>Servicio de Active Directory de Microsoft</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-active-directory-service.md">Proveedor de Microsoft OLE DB para el servicio de Active Directory de Microsoft</a></p></td>
</tr>
<tr class="even">
<td><p>Bases de datos de Microsoft Jet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-microsoft-jet.md">Proveedor de Microsoft OLE DB para Microsoft Jet</a></p></td>
</tr>
<tr class="odd">
<td><p>Microsoft SQL Server</p></td>
<td><p><a href="microsoft-ole-db-provider-for-sql-server.md">Proveedor de Microsoft OLE DB para SQL Server</a></p></td>
</tr>
<tr class="even">
<td><p>Bases de datos de Oracle</p></td>
<td><p><a href="microsoft-ole-db-provider-for-oracle.md">Proveedor de Microsoft OLE DB para Oracle</a></p></td>
</tr>
<tr class="odd">
<td><p>Publicación en Internet</p></td>
<td><p><a href="microsoft-ole-db-provider-for-internet-publishing.md">OLE DB Provider for Internet Publishing</a></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-dynamic-properties"></a>Propiedades dinámicas específicas del proveedor

Las colecciones [Properties](properties-collection-ado.md) de los objetos [Connection](connection-object-ado.md), [Command](command-object-ado.md) y [Recordset](recordset-object-ado.md) incluyen propiedades dinámicas específicas del proveedor. Estas propiedades ofrecen información acerca de funciones específicas del proveedor distintas a las propiedades integradas admitidas por ADO.

Después de establecer la conexión y crear estos objetos, utilice el método [Refresh](refresh-method-ado.md) de la colección **Properties** del objeto para obtener la lista de propiedades específicas del proveedor. Consulte la documentación del proveedor y la Referencia del programador de OLE DB para obtener información detallada acerca de estas propiedades dinámicas.

## <a name="service-providers"></a>Proveedores de servicios

Para utilizar un proveedor de servicios, debe proporcionar una palabra clave. También debe ser consciente de las propiedades dinámicas específicas del proveedor asociadas a cada proveedor de servicios. A continuación se ofrecen detalles sobre los proveedores de servicios disponibles en la actualidad desde Microsoft:

- [Servicio de forma de datos de Microsoft para OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)

- [Proveedor de persistencia de Microsoft OLE DB](microsoft-ole-db-persistence-provider-ado-service-provider.md)

- [Proveedor de servicios remotos de Microsoft OLE DB](microsoft-ole-db-remoting-provider-ado-service-provider.md)

## <a name="service-components"></a>Componentes de servicio

El componente de servicios [Servicio de cursores para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) complementa a las funciones de compatibilidad de cursor de los proveedores de datos. También exige una palabra clave y tiene propiedades dinámicas.

Para obtener más información acerca de los proveedores, vea la documentación de Microsoft OLE DB en el paquete Microsoft Data Access Components SDK o visite el [Centro de desarrollo de plataformas de datos](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

## <a name="provider-commands"></a>Comandos de proveedor

Para cada proveedor que se muestra aquí, si las aplicaciones permiten a los usuarios escribir instrucciones SQL como comandos del proveedor, siempre debe validar la entrada del usuario y estar atento a posibles ataques de hackers mediante una instrucción SQL potencialmente peligrosa, como, como parte de la entrada del usuario.


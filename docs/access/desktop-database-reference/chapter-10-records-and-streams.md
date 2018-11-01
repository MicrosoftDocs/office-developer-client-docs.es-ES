---
title: 'Capítulo 10: Registros y flujos'
TOCTitle: 'Chapter 10: Records and Streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c61aef7a4f0cc34f256300304823341c99fb8436
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876970"
---
# <a name="chapter-10-records-and-streams"></a>Capítulo 10: Registros y flujos


**Se aplica a**: Access 2013, Office 2013

ADO proporciona actualmente el objeto [Recordset](recordset-object-ado.md) como medio principal de obtener acceso a información que se encuentra en orígenes de datos, tales como las bases de datos relacionales. No obstante, algunos proveedores admiten los objetos [Record](record-object-ado.md) y [Stream](stream-object-ado.md) como objetos alternativos o complementarios para manipular los datos. Para obtener información más específica sobre el comportamiento del objeto **Recordset**, vea la documentación del proveedor.

## <a name="records"></a>Objetos Record

Los objetos **Record** funcionan básicamente como objetos **Recordset** de una fila. Sin embargo, los **Records** presentan una funcionalidad limitada en comparación con los **Recordsets** y tienen propiedades y métodos diferentes. El origen para los datos de un objeto **Record** puede ser un comando que devuelva una fila de datos desde el proveedor. El uso de objetos **Record** en vez de **Recordset** para recibir los resultados de una consulta que devuelve una fila de datos elimina la sobrecarga de crear instancias del objeto **Recordset** (más complejo).

Los objetos **Record** pueden servir para otro propósito, especialmente con proveedores para orígenes de datos distintos de las bases de datos relacionales tradicionales, tales como [ Microsoft OLE DB Provider for Internet Publishing ](microsoft-ole-db-provider-for-internet-publishing.md). Gran parte de la información que se debe procesar existe no como tablas de bases de datos, sino como mensajes de sistemas de correo electrónico o como archivos de los modernos sistemas de archivos. Los objetos **Record** y **Stream** facilitan el acceso a información almacenada en orígenes distintos de las bases de datos relacionales.

El objeto **Record** puede representar y administrar datos tales como directorios y archivos de un sistema de archivos, o carpetas y mensajes de un sistema de correo electrónico. En estos casos, el origen para el **registro** puede ser la fila actual de un objeto **Recordset** abierto, una dirección URL absoluta o una dirección URL relativa en combinación con un objeto [Connection](connection-object-ado.md) abierto.

Normalmente, un objeto **Recordset** se puede usar para representar un contenedor o un elemento principal de una jerarquía, tal como una carpeta o un directorio. Un **registro** se puede usar para devolver información específica sobre un nodo del contenedor principal, tal como un archivo o documento. La razón principal por la que los objetos **Record** se utilizan para representar este tipo de información es que estos orígenes de datos son heterogéneos. Esto significa que cada **registro** puede tener un conjunto y un número diferente de campos. Los objetos **Recordset** usuales que contienen filas de una base de datos son homogéneos, lo cual significa que cada fila tiene el mismo número y tipo de campos.

Si desea obtener más información acerca del uso del objeto **Record** para procesar datos heterogéneos de proveedores como el Proveedor de publicación en Internet, vea [Uso de ADO para publicación en Internet](using-ado-for-internet-publishing.md).

## <a name="streams"></a>Objetos Stream

El objeto **Stream** proporciona el medio para leer, escribir y administrar una secuencia de bytes. Esta secuencia de bytes puede ser texto o datos binarios, y su tamaño sólo está limitada por los recursos del sistema. Los objetos **Stream** de ADO se suelen utilizar para los propósitos siguientes:

  - Contener el texto o los bytes que componen un archivo o un mensaje (normalmente se utiliza con proveedores tales como el Microsoft OLE DB Provider for Internet Publishing. Si desea obtener más información acerca de este uso de los objetos **Stream**, vea [Uso de ADO para publicación en Internet](using-ado-for-internet-publishing.md).

Un objeto **Stream** se puede abrir sobre:

  - Un archivo simple especificado con una dirección URL.

  - Un campo de un objeto **Record** o un objeto **Recordset** que contiene un objeto **Stream**.

  - La secuencia predeterminada de un objeto **Record** o **Recordset** que representa un directorio o un archivo compuesto.

  - Un campo de recurso que contiene la dirección URL de un archivo simple.

  - Ninguna origen determinado. En este caso, el objeto **Stream** se abre en la memoria. Se pueden escribir datos en él y después guardarlos en otro **Stream** o en un archivo.

  - Un campo BLOB de un objeto **Recordset**.

En este capítulo, se tratan los temas siguientes:

- [Flujos y persistencia](streams-and-persistence.md)

- [Registros y campos proporcionados por el proveedor](records-and-provider-supplied-fields.md)

- [Direcciones URL relativas y absolutas](absolute-and-relative-urls.md)

- [Using ADO for Internet Publishing (ADO)](using-ado-for-internet-publishing.md)
---
title: Record (objeto) (ADO)
TOCTitle: Record Object (ADO)
ms:assetid: 817aaf13-78d4-1134-aa94-997e92077c22
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249557(v=office.15)
ms:contentKeyID: 48545952
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 806b2292b12bededd299a0ef628601589afe0ce9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603143"
---
# <a name="record-object-ado"></a>Record (objeto) (ADO)


**Se aplica a**: Access 2013 | Office 2013

Representa una fila de un objeto [Recordset](recordset-object-ado.md) o el proveedor de datos, o un objeto devuelto por un proveedor de datos semiestructurados, como un archivo o un directorio.

## <a name="remarks"></a>Comentarios

Un objeto **Record** representa una fila de datos y tiene algunas semejanzas conceptuales con un objeto **Recordset** de una fila. Dependiendo de las funcionalidades de su proveedor, los objetos **Record** se pueden devolver directamente desde dicho proveedor en lugar de un objeto **Recordset** de una fila, por ejemplo, cuando se ejecuta una consulta SQL que selecciona sólo una fila. O bien, un objeto **Record** se puede obtener directamente de un objeto **Recordset**. O bien, un objeto **Record** se puede devolver directamente de un proveedor a datos semiestructurados, como el Proveedor OLE DB para Microsoft Exchange.

Puede ver los campos asociados al objeto **Record** mediante la colección [Fields](fields-collection-ado.md) en el objeto **Record**. ADO permite columnas con valores de objetos, como **Recordset**, **SafeArray** y valores escalares en la colección **Fields** de objetos **Record**.

Si el objeto **Record** representa una fila en un objeto **Recordset**, es posible la devolución a ese objeto **Recordset** original con la propiedad [Source](source-property-ado-record.md).

El objeto **Record** también puede ser utilizado por proveedores de datos semiestructurados, como [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), para modelar espacios de nombres con estructura de árbol. Cada nodo del árbol es un objeto **Record** con columnas asociadas. Las columnas pueden representar los atributos de ese nodo y otro tipo de información correspondiente. El objeto **Record** puede representar tanto un nodo hoja como un nodo que no es hoja en la estructura de árbol. Los nodos que no son hoja tienen otros nodos como contenido, mientras que los nodos hoja no tienen dicho contenido. Los nodos hoja contienen normalmente secuencias binarias de datos, mientras que los nodos que no son hoja también pueden tener asociada una secuencia binaria predeterminada. Las propiedades del objeto **Record** identifican el tipo de nodo.

El objeto **Record** también representa un medio alternativo para desplazarse por datos organizados jerárquicamente. Un objeto **Record** se puede crear para representar la raíz de un subárbol específico en una estructura de árbol de gran tamaño, y los objetos **Record** nuevos se pueden abrir para representar nodos secundarios.

Un recurso (por ejemplo, un archivo o un directorio) puede ser identificado de forma exclusiva por una dirección URL absoluta. Un objeto [Connection](connection-object-ado.md) se crea y establece implícitamente en el objeto **Record** cuando el objeto **Record** se abre con una dirección URL absoluta. Un objeto **Connection** se puede establecer explícitamente en el objeto **Record** mediante la propiedad [ActiveConnection](activeconnection-property-ado.md). Los archivos y directorios accesibles mediante el objeto **Connection** definen el *contexto* en el que pueden producirse operaciones de **registro** .

La modificación de datos y los métodos de desplazamiento en el objeto **Record** también aceptan una dirección URL relativa, que localiza un recurso utilizando una dirección URL absoluta o el contexto del objeto **Connection** como punto inicial.

<<<<<<< HEAD

> [!NOTE]
> <P>[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</P>
=======
> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).
>>>>>>> master



Cada objeto **Record** tiene asociado un objeto **Connection**. Por lo tanto, las operaciones de objetos **Record** pueden formar parte de una transacción mediante la llamada a métodos de transacción de objetos **Connection**.

El objeto **Record** no admite eventos de ADO y, por lo tanto, no responderá a notificaciones.

Con los métodos y las propiedades de un objeto **Record**, se puede hacer lo siguiente:

  - Establecer o devolver el objeto **Connection** asociado con la propiedad [ActiveConnection](activeconnection-property-ado.md).

  - Indicar permisos de acceso con la propiedad [Mode](mode-property-ado.md).

  - Devolver la dirección URL del directorio, si existe, que contiene el recurso representado por el objeto **Record** con la propiedad [ParentURL](parenturl-property-ado.md).

  - Indicar la dirección URL absoluta, la dirección URL relativa o el objeto **Recordset** del que se deriva el objeto **Record** con la propiedad [Source](source-property-ado-record.md).

  - Indicar el estado actual del objeto **Record** con la propiedad [ State ](state-property-ado.md).

  - Indicar el tipo de objeto **Record**, *simple*, *colección* o *documento estructurado*, con la propiedad [RecordType](recordtype-property-ado.md).

  - Detener la ejecución de una operación asincrónica con el método [Cancel](cancel-method-ado.md).

  - Disociar el objeto **Record** de un origen de datos con el método [Close](close-method-ado.md).

  - Copiar el archivo o el directorio representado por un objeto **Record** en otra ubicación con el método [CopyRecord](copyrecord-method-ado.md).

  - Eliminar el archivo, o el directorio y subdirectorios, representado por un objeto **Record** con el método [DeleteRecord](deleterecord-method-ado.md).

  - Abrir un objeto **Recordset** que contenga filas que representen los subdirectorios y archivos de la entidad representada por el objeto **Record** con el método [GetChildren](getchildren-method-ado.md).

  - Mover (cambiar el nombre) el archivo, o el directorio y subdirectorios, representado por un objeto **Record** a otra ubicación con el método [MoveRecord](moverecord-method-ado.md).

  - Asociar el objeto **Record** a un origen de datos existente, o crear un nuevo archivo o directorio con el método [Open](open-method-ado-record.md).


---
title: ActiveConnection (propiedad, ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d3f2a3cf85f51ac4a0d358fcc26e992d61fedca2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886028"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica a qué objeto [Connection](connection-object-ado.md) pertenece actualmente el objeto [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) o [Record](record-object-ado.md) especificado.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String** que contiene la definición de una conexión si la conexión está cerrada, o bien, **Variant** que contiene el actual objeto **Connection** si la conexión está abierta. El valor predeterminado es una referencia de objeto nula. Vea la propiedad [ConnectionString](connectionstring-property-ado.md).

## <a name="remarks"></a>Comentarios

Use la propiedad **ActiveConnection** para determinar el objeto **Connection** a través del cual se va a ejecutar el objeto **Command** especificado o se va a abrir el objeto **Recordset** especificado.

### <a name="command"></a>Comando

Para los objetos **Command**, la propiedad **ActiveConnection** es de lectura y de escritura.

Si se intenta llamar al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) en un objeto **Command** antes de que se establezca esta propiedad en un objeto **Connection** abierto o una cadena de conexión válida, se produce un error.

**Microsoft Visual Basic**: establecer la propiedad **ActiveConnection** en *Nothing* desasocia el objeto **Command** de la actual **conexión** y hace que el proveedor liberar todos los recursos asociados en los datos origen. A continuación, se puede asociar el objeto **Command** al mismo objeto **Connection** o a otro. Algunos proveedores permiten cambiar el valor de la propiedad de una **conexión** a otro, sin tener que establecer primero la propiedad en *Nothing*.

Si la colección [Parameters](parameters-collection-ado.md) del objeto **Command** contiene parámetros proporcionados por el proveedor, se borra la colección si se establece la propiedad **ActiveConnection** en *Nothing* o en otro objeto de **conexión** . Si manualmente crear objetos [Parameter](parameter-object-ado.md) y usarlos para rellenar la colección **Parameters** del objeto **Command** , establecer **ActiveConnection** deja propiedad en *Nothing* o en otro objeto de **conexión** la colección **Parameters** intacta.

Al cerrar el objeto **Connection** al que está asociado un objeto *Command*, el valor de la propiedad **ActiveConnection** se establece en **Nothing**. Si se establece esta propiedad en un objeto **Connection** cerrado, se genera un error.

### <a name="recordset"></a>Recordset

Para los objetos **Recordset** abiertos u objetos **Recordset** cuya propiedad [Source](source-property-ado-recordset.md) está establecida en un objeto **Command** válido, la propiedad **ActiveConnection** es de sólo lectura. En caso contrario, es de lectura y escritura.

Esta propiedad se puede establecer en un objeto **Connection** válido o en una cadena de conexión válida. En este caso, el proveedor crea un nuevo objeto **Connection** mediante esta definición y abre la conexión. Además, el proveedor puede establecer esta propiedad en el nuevo objeto **Connection** para permitir al usuario obtener acceso al objeto **Connection** con el fin de obtener amplia información de errores o ejecutar otros comandos.

Si utiliza el argumento *ActiveConnection* del método [Open](open-method-ado-recordset.md) para abrir un objeto **Recordset** , la propiedad **ActiveConnection** heredará el valor del argumento.

Si se establece la propiedad **Source** del objeto **Recordset** en una variable del objeto **Command**, la propiedad **ActiveConnection** del objeto **Recordset** hereda el valor de la propiedad **ActiveConnection** del objeto **Command**.

**Uso del servicio de datos remoto**: cuando se usa en un objeto Recordset de cliente, esta propiedad puede establecerse sólo en una cadena de conexión o (en Microsoft Visual Basic o Visual Basic Scripting Edition) en *Nothing*.

### <a name="record"></a>Record

Esta propiedad es de lectura y escritura cuando el objeto **Record** está cerrado, y puede contener una cadena de conexión o una referencia a un objeto **Connection** abierto. Esta propiedad es de sólo lectura cuando el objeto **Record** está abierto, y contiene una referencia a un objeto **Connection** abierto.

Se crea implícitamente un objeto **Connection** cuando se abre el objeto **Record** desde una dirección URL. Abra el objeto **Record** con un objeto **Connection** existente abierto asignando el objeto **Connection** a esta propiedad o utilizando el objeto **Connection** como parámetro en la llamada al método [Open](open-method-ado-record.md). Si el **registro** se abre desde un objeto **Record** o [Recordset](recordset-object-ado.md)existente, se asocia automáticamente con objeto de **conexión** de ese objeto **Record** o **Recordset** .

> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).




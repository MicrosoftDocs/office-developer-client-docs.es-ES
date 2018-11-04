---
title: MoveRecord (método, ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 296232b05041c1e059b5134fdde11fceac4e3d43
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949897"
---
# <a name="moverecord-method-ado"></a>MoveRecord (método, ADO)

**Se aplica a**: Access 2013, Office 2013
 
Mueve a otra ubicación la entidad representada por un objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Registro*. MoveRecord (*origen*, *destino*, *nombre de usuario*, *contraseña*, *Opciones*, *Async*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **String** con una dirección URL que identifica el objeto **Record** que se va a mover. Si se omite *Source* o se especifica una cadena vacía, se mueve el objeto representado por este objeto **Record**. Por ejemplo, si el objeto **Record** representa un archivo, el contenido del archivo se mueve hacia la ubicación especificada por *Destination*.|
|*Destination* |Es opcional. Un valor de **tipo String** que contiene una dirección URL que especifica la ubicación donde se va a mover *Source* .|
|*UserName* |Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.|
|*Password* |Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.|
|*Options* |Es opcional. Valor de [MoveRecordOptionsEnum](moverecordoptionsenum.md), cuyo valor predeterminado es **adMoveUnspecified**. Especifica el comportamiento de este método.|
|*Async* |Es opcional. Valor **booleano** que, cuando se especifica **True**, esta operación debe ser asincrónica.|

## <a name="return-value"></a>Valor devuelto

Valor de tipo **String**. Normalmente, se devuelve el valor de *destino* . Sin embargo, el valor devuelto exacto depende del proveedor.

## <a name="remarks"></a>Comentarios

Los valores de *origen* y de *destino* no pueden ser idénticos; de lo contrario, se produce un error en tiempo de ejecución. Al menos los nombres de servidor, ruta de acceso o recurso deben ser diferentes.

En el caso de los archivos que se mueven mediante el proveedor de publicaciones en Internet, este método actualiza todos los vínculos de hipertexto en los archivos que se están moviendo, a menos que se especifique lo contrario en *Options*. Este método genera un error si *Destination* identifica un objeto existente (por ejemplo, un archivo o directorio), a menos que se especifique **adMoveOverWrite**.


> [!NOTE]
> <P>[!NOTA] Utilice la opción <STRONG>adMoveOverWrite</STRONG> con criterio. Por ejemplo, si especifica esta opción cuando mueve un archivo a un directorio, se eliminará el directorio y se reemplazará con el archivo.</P>



Algunos atributos del objeto **Record**, como la propiedad [ParentURL](parenturl-property-ado.md), no se actualizarán tras finalizar esta operación. Actualice las propiedades del objeto **Record** cerrando el objeto **Record** y abriéndolo de nuevo con la dirección URL de la ubicación a la que se ha movido el archivo o directorio.

Si este objeto **Record** se ha obtenido de un objeto [Recordset](recordset-object-ado.md), la nueva ubicación del archivo o directorio que se ha movido no se reflejará inmediatamente en el objeto **Recordset**. Actualice el objeto **Recordset** cerrando y abriéndolo de nuevo.


> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).



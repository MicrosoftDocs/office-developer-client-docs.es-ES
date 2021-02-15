---
title: Método MoveRecord (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288682"
---
# <a name="moverecord-method-ado"></a>Método MoveRecord (ADO)

**Se aplica a:** Access 2013, Office 2013
 
Mueve a otra ubicación la entidad representada por un objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Record*. MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **String** con una dirección URL que identifica el objeto **Record** que se va a mover. Si se omite *Source* o se especifica una cadena vacía, se mueve el objeto representado por este objeto **Record**. Por ejemplo, si el objeto **Record** representa un archivo, el contenido del archivo se mueve hacia la ubicación especificada por *Destination*.|
|*Destination* |Es opcional. Valor de tipo **String** con la dirección URL que especifica la ubicación a la que se va a mover *Source*.|
|*UserName* |Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Destination*.|
|*Password* |Opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.|
|*Options* |Es opcional. Valor de [MoveRecordOptionsEnum](moverecordoptionsenum.md), cuyo valor predeterminado es **adMoveUnspecified**. Especifica el comportamiento de este método.|
|*Async* |Es opcional. Un **valor** booleano que, cuando **es True**, especifica que esta operación debe ser asincrónica.|

## <a name="return-value"></a>Valor devuelto

Valor de tipo **String**. Normalmente se devuelve el valor de *Destination*. Sin embargo, el valor devuelto exacto depende del proveedor.

## <a name="remarks"></a>Comentarios

Los valores de *Source* y *Destination* no pueden ser idénticos; en caso contrario, se produce un error en tiempo de ejecución. Al menos los nombres de servidor, ruta de acceso o recurso deben ser diferentes.

En el caso de los archivos que se mueven mediante el proveedor de publicaciones en Internet, este método actualiza todos los vínculos de hipertexto en los archivos que se están moviendo, a menos que se especifique lo contrario en *Options*. Este método genera un error si *Destination* identifica un objeto existente (por ejemplo, un archivo o directorio), a menos que se especifique **adMoveOverWrite**.

> [!NOTE]
> [!NOTA] Utilice la opción **adMoveOverWrite** con criterio. Por ejemplo, si especifica esta opción cuando mueve un archivo a un directorio, se eliminará el directorio y se reemplazará con el archivo.

Algunos atributos del objeto **Record**, como la propiedad [ParentURL](parenturl-property-ado.md), no se actualizarán tras finalizar esta operación. Actualice las propiedades del objeto **Record** cerrando el objeto **Record** y abriéndolo de nuevo con la dirección URL de la ubicación a la que se ha movido el archivo o directorio.

Si este objeto **Record** se ha obtenido de un objeto [Recordset](recordset-object-ado.md), la nueva ubicación del archivo o directorio que se ha movido no se reflejará inmediatamente en el objeto **Recordset**. Actualice el objeto **Recordset** cerrando y abriéndolo de nuevo.

> [!NOTE]
> [!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Direcciones URL absolutas y relativas.](absolute-and-relative-urls.md)



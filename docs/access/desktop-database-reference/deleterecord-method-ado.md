---
title: Método DeleteRecord (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293997"
---
# <a name="deleterecord-method-ado"></a>Método DeleteRecord (ADO)

**Se aplica a:** Access 2013, Office 2013

Elimina la entidad representada por un objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Record*.**DeleteRecord***Source*, *Async*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **String** con una dirección URL que identifica la entidad (por ejemplo, un archivo o directorio) que se va a eliminar. Si se omite *Source* o se especifica una cadena vacía, se elimina la entidad representada por el actual objeto [Record](record-object-ado.md). Si el objeto Record es un registro de colección (el valor de [RecordType](recordtype-property-ado.md) es **adCollectionRecord**, como un directorio), también se eliminarán todos los objetos secundarios (por ejemplo, subdirectorios).|
|*Async* |Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que la operación de eliminación es asincrónica.|

## <a name="remarks"></a>Comentarios

Puede que las operaciones que se realicen en el objeto representado por este objeto **Record** generen un error después de finalizar este método. Tras llamar a **DeleteRecord**, el objeto **Record** debe estar cerrado porque el comportamiento del objeto **Record** puede volverse impredecible, dependiendo del momento en que el proveedor actualice el objeto **Record** con el origen de datos.

Si este objeto **Record** se obtuvo de un objeto [Recordset](recordset-object-ado.md), los resultados de esta operación no se reflejarán inmediatamente en el objeto **Recordset**. Actualice el **objeto Recordset** cerrando y abriendo de nuevo, o ejecutando los métodos **Recordset** [Requery](requery-method-ado.md)o [Update](update-method-ado.md) y [Resync.](resync-method-ado.md)

> [!NOTE]
> [!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md).



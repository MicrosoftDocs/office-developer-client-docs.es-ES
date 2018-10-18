---
title: DeleteRecord (método, ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a91da1304d399a34f247eb251c2dadf0f1fa94d
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603010"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord (método, ADO)


**Se aplica a**: Access 2013 | Office 2013



Elimina la entidad representada por un objeto [Record](record-object-ado.md).

## <a name="syntax"></a>Sintaxis

*Registro*. **DeleteRecord *** origen*, *Async*

## <a name="parameters"></a>Parámetros

  - *Source*

  - Es opcional. Valor de tipo **String** con una dirección URL que identifica la entidad (por ejemplo, un archivo o directorio) que se va a eliminar. Si se omite *Source* o se especifica una cadena vacía, se elimina la entidad representada por el actual objeto [Record](record-object-ado.md). Si el objeto Record es un registro de colección (el valor de [RecordType](recordtype-property-ado.md) es **adCollectionRecord**, como un directorio), también se eliminarán todos los objetos secundarios (por ejemplo, subdirectorios).

  - *Async*

  - Es opcional. Valor de tipo **Boolean** que, cuando es **True**, especifica que la operación de eliminación es asincrónica.

## <a name="remarks"></a>Comentarios

Puede que las operaciones que se realicen en el objeto representado por este objeto **Record** generen un error después de finalizar este método. Tras llamar a **DeleteRecord**, el objeto **Record** debe estar cerrado porque el comportamiento del objeto **Record** puede volverse impredecible, dependiendo del momento en que el proveedor actualice el objeto **Record** con el origen de datos.

Si este objeto **Record** se obtuvo de un objeto [Recordset](recordset-object-ado.md), los resultados de esta operación no se reflejarán inmediatamente en el objeto **Recordset**. Actualizar el **conjunto de registros** , cierre y vuelva a abrirlo, o mediante la ejecución de los métodos de **Recordset** [Requery](requery-method-ado.md), o [Update](update-method-ado.md) y [Resync](resync-method-ado.md) .


> [!NOTE]
<<<<<<< HEAD
> <P>[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obtener más información, vea <A href="absolute-and-relative-urls.md">Direcciones URL absolutas y relativas</A>.</P>
=======
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).
>>>>>>> master



---
title: Requery (método, ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0105fb67c095355e607c6c73fc73fc4c6b1050ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998199"
---
# <a name="requery-method-ado"></a>Requery (método, ADO)

**Se aplica a**: Access 2013, Office 2013

Actualiza los datos de un objeto [Recordset](recordset-object-ado.md) ejecutando de nuevo la consulta en la que se basa el objeto.

## <a name="syntax"></a>Sintaxis

*conjunto de registros*. Requery *Opciones*

## <a name="parameters"></a>Parámetros

|Nombre |Descripción|
|:----|:----------|
|*Options* |Es opcional. Máscara de bits que contiene valores de [ExecuteOptionEnum](executeoptionenum.md) y [CommandTypeEnum](commandtypeenum.md) que afectan a esta operación.|

> [!NOTE]
> Si *las opciones* está establecido en **adAsyncExecute**, esta operación se ejecutará asincrónicamente y se emitirá un evento [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) cuando finalice.

Los valores de **ExecuteOpenEnum** de **adExecuteNoRecords** o **adExecuteStream** no deben utilizarse con **Requery**.

## <a name="remarks"></a>Comentarios

Utilice el método **Requery** para actualizar todo el contenido de un objeto **Recordset** desde el origen de datos ejecutando de nuevo el comando original y recuperando los datos por segunda vez. Llamar a este método equivale a llamar sucesivamente a los métodos [Close](close-method-ado.md) y [Open](open-method-ado-recordset.md). Si está modificando el registro actual o agregando un registro nuevo, se produce un error.

Mientras esté abierto el objeto **Recordset**, las propiedades que definen la naturaleza del cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), etc.) son de solo lectura. Por lo tanto, el método **Requery** solamente puede actualizar el cursor actual. Para cambiar alguna propiedad del cursor y ver los resultados, debe usar el método [Close](close-method-ado.md) para que las propiedades vuelvan a ser de lectura y escritura. A continuación, podrá cambiar los valores de configuración de las propiedades y llamar al método [Open](open-method-ado-recordset.md) para volver a abrir el cursor.


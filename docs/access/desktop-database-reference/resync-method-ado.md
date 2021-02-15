---
title: Método Resync (ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fa483d86dc345968607a0752f0552ddccfe7fef5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306576"
---
# <a name="resync-method-ado"></a>Método Resync (ADO)

**Se aplica a:** Access 2013, Office 2013

Actualiza los datos del actual objeto [Recordset](recordset-object-ado.md) o la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md) de la base de datos subyacente.

## <a name="syntax"></a>Sintaxis

*Recordset*. Volver a sincronizar *AffectRecords*, *ResyncValues*

*Record*. *Campos*. Volver a sincronizar *ResyncValues*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*AffectRecords* |Es opcional. Un valor de [AffectEnum](affectenum.md) que determina el número de registros que se verán afectados por el método **Resync**. El valor predeterminado es **adAffectAll**. Este valor no está disponible con el método **Resync** de la colección **Fields** de un objeto **Record**.|
|*ResyncValues* |Es opcional. Un valor de [ResyncEnum](resyncenum.md) que especifica si se sobrescriben los valores subyacentes. El valor predeterminado es **adResyncAllValues**.|

## <a name="remarks"></a>Comentarios

### <a name="recordset"></a>Recordset

Use el método **Resync** para volver a sincronizar los registros del actual objeto **Recordset** con la base de datos subyacente. Esto es útil si está usando un cursor estático o de solo avance, pero desea ver todos los cambios en la base de datos subyacente.

Si establece el valor de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient**, **Resync** solo está disponible para los objetos **Recordset** que no sean de solo lectura.

A diferencia del método [Requery](requery-method-ado.md), el método **Resync** no vuelve a ejecutar el comando subyacente del objeto **Recordset**. No se verán los nuevos registros de la base de datos subyacente.

Si un intento de volver a sincronizar genera un error debido a un conflicto con los datos subyacentes (por ejemplo, un registro ha sido eliminado por otro usuario), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) y se produce un error en tiempo de ejecución. Utilice la propiedad [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) y la propiedad [Status](status-property-ado-recordset.md) para localizar los registros con conflictos.

Si están establecidas las propiedades dinámicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y [Resync Command](resync-command-property-dynamic-ado.md), y si el objeto **Recordset** es el resultado de ejecutar una operación de JOIN en varias tablas, el método **Resync** ejecutará el comando especificado en la propiedad **Resync Command** sólo en la tabla indicada en la propiedad **Unique Table**.

### <a name="fields"></a>Fields

Utilice el método **Resync** para volver a sincronizar los valores de la colección **Fields** de un objeto **Record** con el origen de datos subyacente. Este método no afecta a la propiedad [Count](count-property-ado.md).

Si el valor de *ResyncValues* está establecido en **adResyncAllValues** (valor predeterminado), se sincronizan las propiedades [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md) y [OriginalValue](originalvalue-property-ado.md) de los objetos [Field](field-object-ado.md) de la colección. Si el valor de *ResyncValues* está establecido en **adResyncUnderlyingValues**, sólo se sincroniza la propiedad **UnderlyingValue**.

El valor de la propiedad **Status** de cada objeto **Field** en el momento de la llamada también afecta al comportamiento de **Resync**. Para los objetos **Field** cuyo valor de **Status** es **adFieldPendingUnknown** o **adFieldPendingInsert**, **Resync** no tiene ningún efecto. Si **Status** tiene el valor **adFieldPendingChange** o **adFieldPendingDelete**, **Resync** sincroniza los valores de datos de los campos aún existentes en el origen de datos.

**Resync** no modificará los valores de **Status** de los objetos **Field**, a menos que se produzca un error al llamar a **Resync**. Por ejemplo, si ya no existe el campo, el proveedor devolverá un valor de **Status** apropiado para el objeto **Field**, como **adFieldDoesNotExist**. Los valores devueltos de **Status** pueden combinarse lógicamente dentro del valor de la propiedad **Status**.


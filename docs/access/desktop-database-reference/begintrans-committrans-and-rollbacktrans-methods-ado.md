---
title: BeginTrans, CommitTrans y RollbackTrans (métodos, ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d9dc28bd64966e85d16ee2d8cb62fdebc3ba942
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720334"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>BeginTrans, CommitTrans y RollbackTrans (métodos, ADO)

**Se aplica a**: Access 2013, Office 2013

Estos métodos de transacción administran el procesamiento de las transacciones en un objeto [Connection](connection-object-ado.md) de la siguiente manera:

- **BeginTrans**: inicia una transacción nueva.

- **CommitTrans**: guarda los cambios y termina la transacción actual. También puede iniciar una transacción nueva.

- **RollbackTrans**: cancela los cambios realizados durante la transacción actual y termina la transacción. También puede iniciar una transacción nueva.

## <a name="syntax"></a>Sintaxis

*nivel de* = *objeto*. BeginTrans()

*objeto*. BeginTrans

*objeto*. CommitTrans

*objeto*. RollbackTrans

## <a name="return-value"></a>Valor devuelto

Al método **BeginTrans** se le puede llamar como una función que devuelve una variable **Long** que indica el nivel de anidamiento de la transacción.

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*objeto* |Objeto **Connection**.|

### <a name="connection"></a>Connection

Utilice estos métodos con un objeto **Connection** cuando desee guardar o cancelar una serie de cambios realizados en los datos de origen como una sola unidad. Por ejemplo, para transferir dinero entre cuentas, se resta una cantidad de una de las cuentas y se suma la misma cantidad a la otra. Si alguna de las actualizaciones no se realiza correctamente, las cuentas ya no están equilibradas. Si se realizan estos cambios en una transacción abierta, se garantiza que se llevan a cabo todos los cambios, o bien, que no se lleva a cabo ninguno de los cambios.

> [!NOTE]
> [!NOTA] No todos los proveedores admiten transacciones. Compruebe que la propiedad definida por el proveedor de **DDL de transacción** aparece en la colección de [Propiedades](properties-collection-ado.md) del objeto **Connection** , que indica que el proveedor admite transacciones. Si el proveedor no las admite y se llama a uno de estos métodos, se devolverá un error.

Tras llamarse al método **BeginTrans**, el proveedor ya no confirmará instantáneamente los cambios realizados hasta que se llame a **CommitTrans** o a **RollbackTrans** para finalizar la transacción.

En el caso de los proveedores que aceptan transacciones anidadas, si se llama al método **BeginTrans** en una transacción abierta, se inicia una nueva transacción anidada. El valor devuelto indica el nivel de anidamiento: el valor devuelto "1" indica que se ha abierto una transacción de nivel superior (es decir, la transacción no está anidada dentro de otra transacción); el valor devuelto "2" indica que se ha abierto una transacción de segundo nivel (es decir, una transacción anidada dentro de una transacción de nivel superior), y así sucesivamente. Las llamadas a **CommitTrans** o **RollbackTrans** afectan sólo a la última transacción abierta. Es preciso cerrar o deshacer la transacción actual para poder resolver las transacciones de nivel superior.

Si se llama al método **CommitTrans**, se guardan los cambios realizados en una transacción abierta en la conexión y finaliza la transacción. Si se llama al método **RollbackTrans**, se deshacen los cambios realizados en una transacción abierta y finaliza la transacción. Si se llama a cualquiera de los métodos cuando no hay ninguna transacción abierta, se genera un error.

Dependiendo de la propiedad **Attributes** del objeto [Connection](attributes-property-ado.md), una llamada al método **CommitTrans** o **RollbackTrans** puede iniciar automáticamente una transacción nueva. Si el valor de la propiedad **Attributes** es **adXactCommitRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **CommitTrans**. Si el valor de la propiedad **Attributes** es **adXactAbortRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **RollbackTrans**.

### <a name="remote-data-service"></a>Servicio de datos remotos (RDS)

Los métodos **BeginTrans**, **CommitTrans** y **RollbackTrans** no están disponibles en un objeto **Connection** de cliente.


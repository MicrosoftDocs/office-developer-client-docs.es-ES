---
title: Métodos BeginTrans, CommitTrans y RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3de31156f9c06d3a14e7dbef2748543a3e6c4fd
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605761"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a>Métodos BeginTrans, CommitTrans y RollbackTrans (ADO)


**Se aplica a**: Access 2013 | Office 2013


Estos métodos de transacción administran el procesamiento de las transacciones en un objeto [Connection](connection-object-ado.md) de la siguiente manera:

  - **BeginTrans**: inicia una transacción nueva.

  - **CommitTrans**: guarda los cambios y termina la transacción actual. También puede iniciar una transacción nueva.

  - **RollbackTrans**: cancela los cambios realizados durante la transacción actual y termina la transacción. También puede iniciar una transacción nueva.

## <a name="syntax"></a>Sintaxis

*nivel de* = *objeto*. BeginTrans()

*objeto*. BeginTrans

*objeto*. CommitTrans

*objeto*. RollbackTrans

<<<<<<< HEAD
## <a name="return-value"></a>Valor devuelto
=======
## <a name="return-value"></a>Valor devuelto
>>>>>>> master

Al método **BeginTrans** se le puede llamar como una función que devuelve una variable **Long** que indica el nivel de anidamiento de la transacción.

## <a name="parameters"></a>Parámetros

  - *objeto*

  - Objeto **Connection**.

**Connection**

Utilice estos métodos con un objeto **Connection** cuando desee guardar o cancelar una serie de cambios realizados en los datos de origen como una sola unidad. Por ejemplo, para transferir dinero entre cuentas, se resta una cantidad de una de las cuentas y se suma la misma cantidad a la otra. Si alguna de las actualizaciones no se realiza correctamente, las cuentas ya no están equilibradas. Si se realizan estos cambios en una transacción abierta, se garantiza que se llevan a cabo todos los cambios, o bien, que no se lleva a cabo ninguno de los cambios.


> [!NOTE]
> <P>No todos los proveedores admiten transacciones. Compruebe que la propiedad definida por el proveedor "<STRONG>Transaction DDL</STRONG>" aparece en la colección <A href="properties-collection-ado.md">Properties</A> del objeto <STRONG>Connection</STRONG>, lo que indica que el proveedor admite transacciones. Si el proveedor no las admite y se llama a uno de estos métodos, se devolverá un error.</P>



Tras llamarse al método **BeginTrans**, el proveedor ya no confirmará instantáneamente los cambios realizados hasta que se llame a **CommitTrans** o a **RollbackTrans** para finalizar la transacción.

En el caso de los proveedores que aceptan transacciones anidadas, si se llama al método **BeginTrans** en una transacción abierta, se inicia una nueva transacción anidada. El valor devuelto indica el nivel de anidamiento: el valor devuelto "1" indica que se ha abierto una transacción de nivel superior (es decir, la transacción no está anidada dentro de otra transacción); el valor devuelto "2" indica que se ha abierto una transacción de segundo nivel (es decir, una transacción anidada dentro de una transacción de nivel superior), y así sucesivamente. Las llamadas a **CommitTrans** o **RollbackTrans** afectan sólo a la última transacción abierta. Es preciso cerrar o deshacer la transacción actual para poder resolver las transacciones de nivel superior.

Si se llama al método **CommitTrans**, se guardan los cambios realizados en una transacción abierta en la conexión y finaliza la transacción. Si se llama al método **RollbackTrans**, se deshacen los cambios realizados en una transacción abierta y finaliza la transacción. Si se llama a cualquiera de los métodos cuando no hay ninguna transacción abierta, se genera un error.

Dependiendo de la propiedad **Attributes** del objeto [Connection](attributes-property-ado.md), una llamada al método **CommitTrans** o **RollbackTrans** puede iniciar automáticamente una transacción nueva. Si el valor de la propiedad **Attributes** es **adXactCommitRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **CommitTrans**. Si el valor de la propiedad **Attributes** es **adXactAbortRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **RollbackTrans**.

**Servicio de datos remotos (RDS)**

Los métodos **BeginTrans**, **CommitTrans** y **RollbackTrans** no están disponibles en un objeto **Connection** de cliente.


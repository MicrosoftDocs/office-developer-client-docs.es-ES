---
title: Procesamiento de transacciones
TOCTitle: Transaction Processing
ms:assetid: 7cacf3bb-e523-8739-f9ff-c8663c9ddfeb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249523(v=office.15)
ms:contentKeyID: 48545842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f16ae14bc468ce1d96b924faa04bb9a315cab708
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946268"
---
# <a name="transaction-processing"></a>Procesamiento de transacciones


**Se aplica a**: Access 2013, Office 2013

ADO proporciona los siguientes métodos para controlar transacciones: **BeginTrans**, **CommitTrans** y **RollbackTrans**. Utilice estos métodos con un objeto **Connection** cuando desee guardar o cancelar una serie de cambios realizados en los datos de origen como una sola unidad. Por ejemplo, para transferir dinero entre cuentas, se resta una cantidad de una de las cuentas y se suma la misma cantidad a la otra. Si alguna de las actualizaciones no se realiza correctamente, las cuentas ya no están equilibradas. Si se realizan estos cambios en una transacción abierta, se garantiza que se llevan a cabo todos los cambios, o bien, que no se lleva a cabo ninguno de los cambios.


> [!NOTE]
> <P>No todos los proveedores admiten transacciones. Compruebe que la propiedad definida por el proveedor "<STRONG>Transaction DDL</STRONG>" aparece en la colección <A href="properties-collection-ado.md">Properties</A> del objeto <STRONG>Connection</STRONG>, lo que indica que el proveedor admite transacciones. Si el proveedor no las admite y se llama a uno de estos métodos, se devolverá un error.</P>



Después de llamar al método **BeginTrans**, el proveedor ya no confirmará instantáneamente los cambios realizados hasta que se llame a **CommitTrans** o a **RollbackTrans** para finalizar la transacción.

Si se llama al método **CommitTrans**, se guardan los cambios realizados en una transacción abierta en la conexión y finaliza la transacción. Si se llama al método **RollbackTrans**, se deshacen los cambios realizados en una transacción abierta y finaliza la transacción. Si se llama a cualquiera de los métodos cuando no hay ninguna transacción abierta, se genera un error.

En función de la propiedad **Attributes** del objeto [Connection](attributes-property-ado.md), una llamada a los métodos **CommitTrans** o **RollbackTrans** puede iniciar automáticamente una transacción nueva. Si el valor de la propiedad **Attributes** es **adXactCommitRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **CommitTrans**. Si el valor de la propiedad **Attributes** es **adXactAbortRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **RollbackTrans**.

## <a name="transaction-isolation-level"></a>Nivel de aislamiento de la transacción

Use la propiedad **IsolationLevel** para establecer el nivel de aislamiento de una transacción en un objeto **Connection**. La configuración no se aplica hasta la siguiente vez que se llame al método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si el nivel de aislamiento solicitado no está disponible, el proveedor puede devolver el nivel superior siguiente de aislamiento. Hacer referencia a la propiedad **IsolationLevel** en la referencia del programador de ADO para obtener más detalles sobre valores válidos.

## <a name="nested-transactions"></a>Transacciones anidadas

En el caso de los proveedores que aceptan transacciones anidadas, si se llama al método **BeginTrans** en una transacción abierta, se inicia una nueva transacción anidada. El valor devuelto indica el nivel de anidamiento: el valor devuelto "1" indica que se ha abierto una transacción de nivel superior (es decir, la transacción no está anidada dentro de otra transacción); el valor devuelto "2" indica que se ha abierto una transacción de segundo nivel (es decir, una transacción anidada dentro de una transacción de nivel superior), etc. Las llamadas a **CommitTrans** o **RollbackTrans** afectan sólo a la última transacción abierta. Es preciso cerrar o deshacer la transacción actual para poder resolver las transacciones de nivel superior.


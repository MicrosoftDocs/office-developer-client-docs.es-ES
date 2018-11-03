---
title: BeginTrans, CommitTrans y RollbackTrans (métodos, ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca7c63e0c310535ecdf84a11c656d00ff436627f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945925"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="8d615-102">BeginTrans, CommitTrans y RollbackTrans (métodos, ADO)</span><span class="sxs-lookup"><span data-stu-id="8d615-102">BeginTrans, CommitTrans, and RollbackTrans methods (ADO)</span></span>

<span data-ttu-id="8d615-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d615-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d615-104">Estos métodos de transacción administran el procesamiento de las transacciones en un objeto [Connection](connection-object-ado.md) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8d615-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

- <span data-ttu-id="8d615-105">**BeginTrans**: inicia una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="8d615-105">**BeginTrans** — Begins a new transaction.</span></span>

- <span data-ttu-id="8d615-p101">**CommitTrans**: guarda los cambios y termina la transacción actual. También puede iniciar una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="8d615-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

- <span data-ttu-id="8d615-p102">**RollbackTrans**: cancela los cambios realizados durante la transacción actual y termina la transacción. También puede iniciar una transacción nueva.</span><span class="sxs-lookup"><span data-stu-id="8d615-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d615-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d615-110">Syntax</span></span>

<span data-ttu-id="8d615-111">*nivel de* = *objeto*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="8d615-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="8d615-112">*objeto*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="8d615-112">*object*.BeginTrans</span></span>

<span data-ttu-id="8d615-113">*objeto*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="8d615-113">*object*.CommitTrans</span></span>

<span data-ttu-id="8d615-114">*objeto*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="8d615-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="8d615-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d615-115">Return value</span></span>

<span data-ttu-id="8d615-116">Al método **BeginTrans** se le puede llamar como una función que devuelve una variable **Long** que indica el nivel de anidamiento de la transacción.</span><span class="sxs-lookup"><span data-stu-id="8d615-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d615-117">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d615-117">Parameters</span></span>

- <span data-ttu-id="8d615-118">*objeto*</span><span class="sxs-lookup"><span data-stu-id="8d615-118">*object*</span></span>

  - <span data-ttu-id="8d615-119">Objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="8d615-119">A **Connection** object.</span></span>

### <a name="connection"></a><span data-ttu-id="8d615-120">Connection</span><span class="sxs-lookup"><span data-stu-id="8d615-120">Connection</span></span>

<span data-ttu-id="8d615-p103">Utilice estos métodos con un objeto **Connection** cuando desee guardar o cancelar una serie de cambios realizados en los datos de origen como una sola unidad. Por ejemplo, para transferir dinero entre cuentas, se resta una cantidad de una de las cuentas y se suma la misma cantidad a la otra. Si alguna de las actualizaciones no se realiza correctamente, las cuentas ya no están equilibradas. Si se realizan estos cambios en una transacción abierta, se garantiza que se llevan a cabo todos los cambios, o bien, que no se lleva a cabo ninguno de los cambios.</span><span class="sxs-lookup"><span data-stu-id="8d615-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>

> [!NOTE]
> <span data-ttu-id="8d615-p104">No todos los proveedores admiten transacciones. Compruebe que la propiedad definida por el proveedor "**Transaction DDL**" aparece en la colección [Properties](properties-collection-ado.md) del objeto **Connection**, lo que indica que el proveedor admite transacciones. Si el proveedor no las admite y se llama a uno de estos métodos, se devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="8d615-p104">Not all providers support transactions. Verify that the provider-defined property "**Transaction DDL**" appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="8d615-128">Tras llamarse al método **BeginTrans**, el proveedor ya no confirmará instantáneamente los cambios realizados hasta que se llame a **CommitTrans** o a **RollbackTrans** para finalizar la transacción.</span><span class="sxs-lookup"><span data-stu-id="8d615-128">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="8d615-p105">En el caso de los proveedores que aceptan transacciones anidadas, si se llama al método **BeginTrans** en una transacción abierta, se inicia una nueva transacción anidada. El valor devuelto indica el nivel de anidamiento: el valor devuelto "1" indica que se ha abierto una transacción de nivel superior (es decir, la transacción no está anidada dentro de otra transacción); el valor devuelto "2" indica que se ha abierto una transacción de segundo nivel (es decir, una transacción anidada dentro de una transacción de nivel superior), y así sucesivamente. Las llamadas a **CommitTrans** o **RollbackTrans** afectan sólo a la última transacción abierta. Es preciso cerrar o deshacer la transacción actual para poder resolver las transacciones de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8d615-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="8d615-p106">Si se llama al método **CommitTrans**, se guardan los cambios realizados en una transacción abierta en la conexión y finaliza la transacción. Si se llama al método **RollbackTrans**, se deshacen los cambios realizados en una transacción abierta y finaliza la transacción. Si se llama a cualquiera de los métodos cuando no hay ninguna transacción abierta, se genera un error.</span><span class="sxs-lookup"><span data-stu-id="8d615-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="8d615-p107">Dependiendo de la propiedad **Attributes** del objeto [Connection](attributes-property-ado.md), una llamada al método **CommitTrans** o **RollbackTrans** puede iniciar automáticamente una transacción nueva. Si el valor de la propiedad **Attributes** es **adXactCommitRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **CommitTrans**. Si el valor de la propiedad **Attributes** es **adXactAbortRetaining**, el proveedor inicia automáticamente una transacción nueva después de una llamada a **RollbackTrans**.</span><span class="sxs-lookup"><span data-stu-id="8d615-p107">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

### <a name="remote-data-service"></a><span data-ttu-id="8d615-138">Servicio de datos remotos (RDS)</span><span class="sxs-lookup"><span data-stu-id="8d615-138">Remote Data Service</span></span>

<span data-ttu-id="8d615-139">Los métodos **BeginTrans**, **CommitTrans** y **RollbackTrans** no están disponibles en un objeto **Connection** de cliente.</span><span class="sxs-lookup"><span data-stu-id="8d615-139">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>


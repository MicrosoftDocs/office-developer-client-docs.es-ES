---
title: LockType (propiedad, ADO)
TOCTitle: LockType Property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d1740f42fae3485d88a4820081621f7f2483c51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485970"
---
# <a name="locktype-property-ado"></a>LockType (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el tipo de bloqueos colocados en registros durante la modificación.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [LockTypeEnum](locktypeenum.md). El valor predeterminado es **adLockReadOnly**.

## <a name="remarks"></a>Comentarios

Establezca la propiedad **LockType** antes de abrir un objeto [Recordset](recordset-object-ado.md) a fin de especificar el tipo de bloqueo que el proveedor debe usar al abrirlo. Lea la propiedad para devolver el tipo de bloqueo en uso a un objeto **Recordset**.

Es posible que los proveedores no admitan todos los tipos de bloqueo. Si un proveedor no puede admitir el valor **LockType** solicitado, lo sustituirá por otro tipo de bloqueo. Para determinar la funcionalidad de bloqueo real disponible en un objeto **Recordset**, use el método [Supports](supports-method-ado.md) con **adUpdate** y **adUpdateBatch**.

No se admite el valor **adLockPessimistic** cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**. Si se establece un valor no admitido, no se producirá ningún error; se utilizará el valor admitido de **LockType** más cercano.

La propiedad **LockType** es de lectura y escritura cuando el objeto **Recordset** está cerrado y de sólo lectura cuando está abierto.

**Uso de servicio de datos remotos** Cuando se usa en un objeto Recordset de cliente, sólo puede establecerse la propiedad **LockType** en **adLockBatchOptimistic**.


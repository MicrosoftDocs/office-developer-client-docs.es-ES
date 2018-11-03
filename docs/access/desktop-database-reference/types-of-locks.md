---
title: Tipos de bloqueos (referencia de escritorio de la base de datos de Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a104b2ad452cdf8b0688dbc84ca09b90ed08c62
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944917"
---
# <a name="types-of-locks"></a>Tipos de bloqueos


**Se aplica a**: Access 2013, Office 2013



## <a name="adlockbatchoptimistic"></a>adLockBatchOptimistic

Indica actualizaciones optimistas por lotes. Se requiere para el modo de actualización por lotes.

Muchas aplicaciones recuperan muchas filas a la vez y deben efectuar, a continuación, actualizaciones coordinadas que incluyen el conjunto completo de filas que se van a insertar, actualizar o eliminar. Con cursores por lotes, sólo es necesario un viaje de ida y vuelta al servidor, mejorando así el rendimiento de la actualización y reduciendo el tráfico de red. Mediante el uso de una biblioteca de cursores por lotes puede crear un cursor estático y, a continuación, desconectar del origen de datos. En este punto, puede realizar cambios en las filas y, posteriormente, volver a conectarse y enviar los cambios al origen de datos en un lote.

## <a name="adlockoptimistic"></a>adLockOptimistic

Indica que el proveedor utiliza bloqueo optimista, bloqueando registros sólo cuando se llama al método **Update**. Es decir, existe una posibilidad de que los datos los pueda modificar otro usuario entre el instante en que se modificó el registro y el momento en que se llama a **Update**, algo que crea conflictos. Utilice este tipo de bloqueo en situaciones en las que son pocas las posibilidades de que se produzca un conflicto o cuando los conflictos se puedan resolver fácilmente.

## <a name="adlockpessimistic"></a>adLockPessimistic

Indica un bloqueo pesimista, registro por registro. El proveedor realiza las acciones necesarias para garantizar la modificación correcta de los registros, normalmente bloqueando los registros en el origen de datos inmediatamente antes de la modificación. Por supuesto, esto significa que los registros no están disponibles para otros usuarios una vez que se empieza a modificar hasta que se libera el bloqueo llamando a **Update**. Utilice este tipo de bloqueo en un sistema donde no se pueden permitir cambios concurrentes en los datos (por ejemplo, un sistema de reservas).

## <a name="adlockreadonly"></a>adLockReadOnly

Indica registros de sólo lectura. No es posible alterar los datos. Un bloqueo de sólo lectura es el tipo de bloqueo "más rápido", ya que no requiere que el servidor mantenga un bloqueo sobre los registros.

## <a name="adlockunspecified"></a>adLockUnspecified

No especifica ningún tipo de bloqueo.


---
title: Método Recordset.MoveFirst (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 31d003d7ae98bf509aca8f24da9c37f0276af6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300241"
---
# <a name="recordsetmovefirst-method-dao"></a>Método Recordset.MoveFirst (DAO)


**Se aplica a:** Access 2013, Office 2013

Se desplaza al primer registro de un objeto **Recordset** especificado y convierte ese registro en el registro activo.

## <a name="syntax"></a>Sintaxis

*expression* .MoveFirst

*expression* Variable que representa un objeto **Recordset**.

## <a name="remarks"></a>Comentarios

Use los métodos **Move** para desplazarse de un registro a otro sin aplicar una condición.

Si edita el registro activo, asegúrese de que usa el método **Update** para guardar los cambios antes de moverse a otro registro. Si se desplaza a otro registro sin ejecutar una actualización, los cambios se pierden sin advertencia.

Cuando abre un objeto **Recordset**, el primer registro es el activo y la propiedad **BOF** es **False**. Si **Recordset** no contiene registros, la propiedad **BOF** es **True** y no hay ningún registro activo.

Si el primer o el último registro ya está activo cuando usa **MoveFirst** o **MoveLast**, el registro actual no cambia.

Si recordset hace referencia a un objeto **Recordset** de tipo de tabla (solo en áreas de trabajo de Microsoft Access), el movimiento sigue el índice actual. Puede definir el índice actual mediante la propiedad **Index**. Si no define el índice actual, el orden de los registros devueltos queda sin definir.

No puede usar los métodos **MoveFirst**, **MoveLast** ni **MovePrevious** en un objeto **Recordset** de tipo de solo avance.

Para mover la posición del registro actual en un objeto **Recordset** un número específico de registros hacia delante o hacia atrás, use el método **Move**.


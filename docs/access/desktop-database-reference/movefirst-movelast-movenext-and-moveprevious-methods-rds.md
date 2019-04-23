---
title: Métodos MoveFirst, moVelast, MoveNext y MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288689"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>Métodos MoveFirst, moVelast, MoveNext y MovePrevious (RDS)

**Se aplica a:** Access 2013, Office 2013

Se desplaza al primer, último, siguiente o anterior registro de un objeto [Recordset](recordset-object-ado.md) especificado.

## <a name="syntax"></a>Sintaxis

*DataControl*. Registros. { MoveFirst | MoVelast | MoveNext | MovePrevious

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*DataControl* |Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Comentarios

Puede usar los métodos **Move** con el **objeto RDS. DataControl** para navegar por los registros de datos en los controles enlazados a datos de una página web. 

Por ejemplo, supongamos que muestra un objeto **Recordset** en una cuadrícula enlazando a un objeto **RDS.DataControl**. A continuación, podrá incluir los botones Primero, Último, Siguiente y Anterior, en los que los usuarios pueden hacer clic para moverse hacia el registro primero, último, siguiente o anterior del objeto **Recordset** mostrado. Para ello, debe llamar a los métodos **MoveFirst**, **MoveLast**, **MoveNext** y **MovePrevious** del objeto **RDS.DataControl** en los procedimientos onClick de los botones Primero, Último, Siguiente y Anterior, respectivamente. En el [Ejemplo de la Libreta de direcciones](address-book-navigation-buttons.md) se muestra cómo hacerlo.


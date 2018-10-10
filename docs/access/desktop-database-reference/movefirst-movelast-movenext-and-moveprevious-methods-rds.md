---
title: Métodos MoveFirst, MoveLast, MoveNext y MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485216"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>Métodos MoveFirst, MoveLast, MoveNext y MovePrevious (RDS)


**Se aplica a**: Access 2013 | Office 2013

Se desplaza al primer, último, siguiente o anterior registro de un objeto [Recordset](recordset-object-ado.md) especificado.

## <a name="syntax"></a>Sintaxis

*DataControl*. Conjunto de registros. { Métodos MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Parámetros

  - *DataControl*

  - Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).

## <a name="remarks"></a>Comentarios

Puede usar los métodos **Move** con el objeto **RDS.DataControl** para navegar por los registros de datos en los controles enlazados a datos de una página Web. Por ejemplo, supongamos que muestra un objeto **Recordset** en una cuadrícula enlazando a un objeto **RDS.DataControl**. A continuación, podrá incluir los botones Primero, Último, Siguiente y Anterior, en los que los usuarios pueden hacer clic para moverse hacia el registro primero, último, siguiente o anterior del objeto **Recordset** mostrado. Para ello, debe llamar a los métodos **MoveFirst**, **MoveLast**, **MoveNext** y **MovePrevious** del objeto **RDS.DataControl** en los procedimientos onClick de los botones Primero, Último, Siguiente y Anterior, respectivamente. En el [Ejemplo de la Libreta de direcciones](address-book-navigation-buttons.md) se muestra cómo hacerlo.


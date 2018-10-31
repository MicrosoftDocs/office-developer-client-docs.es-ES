---
title: Instrucción TRANSACTION (Microsoft Access SQL)
TOCTitle: TRANSACTION statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d93fc90beded30d96b4db54c35ab3046da06899
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862670"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrucción TRANSACTION (Microsoft Access SQL)

**Se aplica a**: Access 2013 | Office 2013

Se usa para iniciar y concluir transacciones explícitas.

## <a name="syntax"></a>Sintaxis

**Iniciar una transacción**:

BEGIN TRANSACTION

**Concluir una transacción y confirmar todos los de trabajo realizado durante la transacción**:

Confirmar \[transacciones | TRABAJO\]

**Concluir una transacción y revertir todo el trabajo realizado durante la transacción**:

REVERSIÓN \[transacciones | TRABAJO\]

## <a name="remarks"></a>Comentarios

Las transacciones no se inician automáticamente. Las transacciones deben iniciarse de forma explícita mediante BEGIN TRANSACTION.

Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.

Las transacciones no se admiten para tablas vinculadas.


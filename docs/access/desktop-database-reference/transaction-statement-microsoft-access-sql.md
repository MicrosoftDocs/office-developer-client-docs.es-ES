---
title: Instrucción TRANSACTION (Microsoft Access SQL)
TOCTitle: TRANSACTION Statement (Microsoft Access SQL)
ms:assetid: 481e807d-94e4-f201-adac-d25ee89d9220
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193241(v=office.15)
ms:contentKeyID: 48544614
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277472
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 13628ee6d384430691475eb06dbbbdce4e980103
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485122"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrucción TRANSACTION (Microsoft Access SQL)


**Se aplica a**: Access 2013 | Office 2013

Se usa para iniciar y concluir transacciones explícitas.

## <a name="syntax"></a>Sintaxis

Para iniciar una transacción:

BEGIN TRANSACTION

Para concluir una transacción y confirmar todo el trabajo realizado durante la misma:

Confirmar \[transacciones | TRABAJO\]

Para concluir una transacción y revertir todo el trabajo realizado durante la misma:

REVERSIÓN \[transacciones | TRABAJO\]

## <a name="remarks"></a>Comentarios

Las transacciones no se inician automáticamente. Las transacciones deben iniciarse de forma explícita mediante BEGIN TRANSACTION.

Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.

Las transacciones no se admiten para tablas vinculadas.


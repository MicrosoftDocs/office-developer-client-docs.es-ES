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
ms.openlocfilehash: f48b1ab98f6f0f729fdb32b4ff20be09c5d942bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886392"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrucción TRANSACTION (Microsoft Access SQL)

**Se aplica a**: Access 2013, Office 2013

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


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
localization_priority: Priority
ms.openlocfilehash: 828bccfad83320d27f9473d532ab86f73b2fde98
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705522"
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


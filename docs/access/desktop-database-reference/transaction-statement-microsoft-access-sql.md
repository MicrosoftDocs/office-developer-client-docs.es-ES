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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314150"
---
# <a name="transaction-statement-microsoft-access-sql"></a>Instrucción TRANSACTION (Microsoft Access SQL)

**Se aplica a:** Access 2013, Office 2013

Se usa para iniciar y finalizar transacciones explícitas.

## <a name="syntax"></a>Sintaxis

**Para iniciar una transacción**:

BEGIN TRANSACTION

**Para concluir una transacción y confirmar todo el trabajo realizado durante la misma**:

COMMIT \[TRANSACTION | WORK\]

**Para concluir una transacción y revertir todo el trabajo realizado durante la misma**:

ROLLBACK \[TRANSACTION | WORK\]

## <a name="remarks"></a>Comentarios

Las transacciones no se inician automáticamente. Para iniciar una transacción, debe hacerlo explícitamente con BEGIN TRANSACTION.

Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.

No se admiten transacciones para tablas vinculadas.


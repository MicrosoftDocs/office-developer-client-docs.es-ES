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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="aaec5-102">Instrucción TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="aaec5-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="aaec5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aaec5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aaec5-104">Se usa para iniciar y finalizar transacciones explícitas.</span><span class="sxs-lookup"><span data-stu-id="aaec5-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaec5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aaec5-105">Syntax</span></span>

<span data-ttu-id="aaec5-106">**Para iniciar una transacción**:</span><span class="sxs-lookup"><span data-stu-id="aaec5-106">Initiate a new transaction.</span></span>

<span data-ttu-id="aaec5-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="aaec5-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="aaec5-108">**Para concluir una transacción y confirmar todo el trabajo realizado durante la misma**:</span><span class="sxs-lookup"><span data-stu-id="aaec5-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="aaec5-109">COMMIT \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="aaec5-109">COMMIT [TRANSACTION | WORK]</span></span>

<span data-ttu-id="aaec5-110">**Para concluir una transacción y revertir todo el trabajo realizado durante la misma**:</span><span class="sxs-lookup"><span data-stu-id="aaec5-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="aaec5-111">ROLLBACK \[TRANSACTION | WORK\]</span><span class="sxs-lookup"><span data-stu-id="aaec5-111">ROLLBACK [TRANSACTION | WORK]</span></span>

## <a name="remarks"></a><span data-ttu-id="aaec5-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aaec5-112">Remarks</span></span>

<span data-ttu-id="aaec5-p101">Las transacciones no se inician automáticamente. Para iniciar una transacción, debe hacerlo explícitamente con BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="aaec5-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="aaec5-p102">Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="aaec5-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="aaec5-117">No se admiten transacciones para tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="aaec5-117">Transactions are not supported for linked tables.</span></span>


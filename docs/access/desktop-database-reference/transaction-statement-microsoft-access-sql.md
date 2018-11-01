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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="db830-102">Instrucción TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="db830-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="db830-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db830-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db830-104">Se usa para iniciar y concluir transacciones explícitas.</span><span class="sxs-lookup"><span data-stu-id="db830-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="db830-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db830-105">Syntax</span></span>

<span data-ttu-id="db830-106">**Iniciar una transacción**:</span><span class="sxs-lookup"><span data-stu-id="db830-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="db830-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="db830-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="db830-108">**Concluir una transacción y confirmar todos los de trabajo realizado durante la transacción**:</span><span class="sxs-lookup"><span data-stu-id="db830-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="db830-109">Confirmar \[transacciones | TRABAJO\]</span><span class="sxs-lookup"><span data-stu-id="db830-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="db830-110">**Concluir una transacción y revertir todo el trabajo realizado durante la transacción**:</span><span class="sxs-lookup"><span data-stu-id="db830-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="db830-111">REVERSIÓN \[transacciones | TRABAJO\]</span><span class="sxs-lookup"><span data-stu-id="db830-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="db830-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db830-112">Remarks</span></span>

<span data-ttu-id="db830-p101">Las transacciones no se inician automáticamente. Las transacciones deben iniciarse de forma explícita mediante BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="db830-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="db830-p102">Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="db830-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="db830-117">Las transacciones no se admiten para tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="db830-117">Transactions are not supported for linked tables.</span></span>


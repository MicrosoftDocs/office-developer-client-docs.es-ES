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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="2c5a4-102">Instrucción TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2c5a4-102">TRANSACTION Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="2c5a4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c5a4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2c5a4-104">Se usa para iniciar y concluir transacciones explícitas.</span><span class="sxs-lookup"><span data-stu-id="2c5a4-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c5a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c5a4-105">Syntax</span></span>

<span data-ttu-id="2c5a4-106">Para iniciar una transacción:</span><span class="sxs-lookup"><span data-stu-id="2c5a4-106">Initiate a new transaction.</span></span>

<span data-ttu-id="2c5a4-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="2c5a4-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="2c5a4-108">Para concluir una transacción y confirmar todo el trabajo realizado durante la misma:</span><span class="sxs-lookup"><span data-stu-id="2c5a4-108">Conclude a transaction by committing all work performed during the transaction.</span></span>

<span data-ttu-id="2c5a4-109">Confirmar \[transacciones | TRABAJO\]</span><span class="sxs-lookup"><span data-stu-id="2c5a4-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="2c5a4-110">Para concluir una transacción y revertir todo el trabajo realizado durante la misma:</span><span class="sxs-lookup"><span data-stu-id="2c5a4-110">Conclude a transaction by rolling back all work performed during the transaction.</span></span>

<span data-ttu-id="2c5a4-111">REVERSIÓN \[transacciones | TRABAJO\]</span><span class="sxs-lookup"><span data-stu-id="2c5a4-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="2c5a4-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2c5a4-112">Remarks</span></span>

<span data-ttu-id="2c5a4-p101">Las transacciones no se inician automáticamente. Las transacciones deben iniciarse de forma explícita mediante BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="2c5a4-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="2c5a4-p102">Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="2c5a4-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="2c5a4-117">Las transacciones no se admiten para tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="2c5a4-117">Transactions are not supported for linked tables.</span></span>


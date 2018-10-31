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
# <a name="transaction-statement-microsoft-access-sql"></a><span data-ttu-id="70d94-102">Instrucción TRANSACTION (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="70d94-102">TRANSACTION statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="70d94-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="70d94-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="70d94-104">Se usa para iniciar y concluir transacciones explícitas.</span><span class="sxs-lookup"><span data-stu-id="70d94-104">Used to initiate and conclude explicit transactions.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70d94-105">Syntax</span></span>

<span data-ttu-id="70d94-106">**Iniciar una transacción**:</span><span class="sxs-lookup"><span data-stu-id="70d94-106">**Initiate a new transaction**:</span></span>

<span data-ttu-id="70d94-107">BEGIN TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="70d94-107">BEGIN TRANSACTION</span></span>

<span data-ttu-id="70d94-108">**Concluir una transacción y confirmar todos los de trabajo realizado durante la transacción**:</span><span class="sxs-lookup"><span data-stu-id="70d94-108">**Conclude a transaction by committing all work performed during the transaction**:</span></span>

<span data-ttu-id="70d94-109">Confirmar \[transacciones | TRABAJO\]</span><span class="sxs-lookup"><span data-stu-id="70d94-109">COMMIT \[TRANSACTION | WORK\]</span></span>

<span data-ttu-id="70d94-110">**Concluir una transacción y revertir todo el trabajo realizado durante la transacción**:</span><span class="sxs-lookup"><span data-stu-id="70d94-110">**Conclude a transaction by rolling back all work performed during the transaction**:</span></span>

<span data-ttu-id="70d94-111">REVERSIÓN \[transacciones | TRABAJO\]</span><span class="sxs-lookup"><span data-stu-id="70d94-111">ROLLBACK \[TRANSACTION | WORK\]</span></span>

## <a name="remarks"></a><span data-ttu-id="70d94-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="70d94-112">Remarks</span></span>

<span data-ttu-id="70d94-p101">Las transacciones no se inician automáticamente. Las transacciones deben iniciarse de forma explícita mediante BEGIN TRANSACTION.</span><span class="sxs-lookup"><span data-stu-id="70d94-p101">Transactions are not started automatically. To start a transaction, you must do so explicitly using BEGIN TRANSACTION.</span></span>

<span data-ttu-id="70d94-p102">Las transacciones se pueden anidar hasta cinco niveles. Para iniciar una transacción anidada, use BEGIN TRANSACTION en el contexto de una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="70d94-p102">Transactions can be nested up to five levels deep. To start a nested transaction, use BEGIN TRANSACTION within the context of an existing transaction.</span></span>

<span data-ttu-id="70d94-117">Las transacciones no se admiten para tablas vinculadas.</span><span class="sxs-lookup"><span data-stu-id="70d94-117">Transactions are not supported for linked tables.</span></span>


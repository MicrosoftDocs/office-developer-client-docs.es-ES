---
title: Recordset2.Cancel (método) (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929237"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="a4704-102">Recordset2.Cancel (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="a4704-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="a4704-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4704-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a4704-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4704-104">Syntax</span></span>

<span data-ttu-id="a4704-105">*expresión* . Cancelar</span><span class="sxs-lookup"><span data-stu-id="a4704-105">*expression* .Cancel</span></span>

<span data-ttu-id="a4704-106">*expresión* Expresión que devuelve un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="a4704-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4704-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4704-107">Remarks</span></span>

<span data-ttu-id="a4704-108">Utilice el método **Cancel** para finalizar la ejecución de una llamada al método **Execute** u **OpenConnection** asincrónica (es decir, el método se abrió con la opción dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="a4704-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="a4704-109">**Cancel** devolverá un error en tiempo de ejecución si no se utilizó dbRunAsync en el método que está intentando terminar.</span><span class="sxs-lookup"><span data-stu-id="a4704-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


---
title: DBEngine.Version Property (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3516a25623b6838286969c51f2d9346321f3326e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483539"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="0c320-102">DBEngine.Version Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0c320-102">DBEngine.Version Property (DAO)</span></span>


<span data-ttu-id="0c320-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c320-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0c320-p101">Devuelve la versión de DAO que se está utilizando. **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0c320-p101">Rreturns the version of DAO currently in use. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c320-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c320-106">Syntax</span></span>

<span data-ttu-id="0c320-107">*expresión* . Versión</span><span class="sxs-lookup"><span data-stu-id="0c320-107">*expression* .Version</span></span>

<span data-ttu-id="0c320-108">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0c320-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c320-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c320-109">Remarks</span></span>

<span data-ttu-id="0c320-p102">El valor devuelto es un tipo de datos String que se evalúa en un número de versión en el formato "major.minor". Por ejemplo, "3.0". El número de versión del producto consta del número de versión (3), un punto y el número de lanzamiento (0).</span><span class="sxs-lookup"><span data-stu-id="0c320-p102">The return value is a String that evaluates to a version number in the form "major.minor". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>


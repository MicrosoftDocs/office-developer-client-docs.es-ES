---
title: Propiedad DBEngine.Version (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 7e22645127f18ad815c398fd38f9ac4615dfadc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294193"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="a7bc2-102">Propiedad DBEngine.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="a7bc2-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="a7bc2-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7bc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7bc2-104">Devuelve la versión de DAO que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-104">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="a7bc2-105">**String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7bc2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7bc2-106">Syntax</span></span>

<span data-ttu-id="a7bc2-107">*expresión* . Versión</span><span class="sxs-lookup"><span data-stu-id="a7bc2-107">*expression* .Version</span></span>

<span data-ttu-id="a7bc2-108">*expression* Variable que representa un objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7bc2-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a7bc2-109">Remarks</span></span>

<span data-ttu-id="a7bc2-110">El valor devuelto es un tipo de datos String que se evalúa en un número de versión en el formato "major.minor".</span><span class="sxs-lookup"><span data-stu-id="a7bc2-110">The return value is a String that evaluates to a version number in the form "major.minor".</span></span> <span data-ttu-id="a7bc2-111">Por ejemplo, "3.0".</span><span class="sxs-lookup"><span data-stu-id="a7bc2-111">For example, "3.0".</span></span> <span data-ttu-id="a7bc2-112">El número de versión del producto consta del número de versión (3), un punto y el número de lanzamiento (0).</span><span class="sxs-lookup"><span data-stu-id="a7bc2-112">The product version number consists of the version number (3), a period, and the release number (0).</span></span>


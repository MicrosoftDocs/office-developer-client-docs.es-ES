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
ms.openlocfilehash: 1723deea7f29c59fb388a11acc5e5ffcced4abe1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924599"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="9cea9-102">Propiedad DBEngine.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="9cea9-102">DBEngine.Version property (DAO)</span></span>


<span data-ttu-id="9cea9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cea9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9cea9-p101">Devuelve la versión de DAO que se está utilizando. **String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="9cea9-p101">Rreturns the version of DAO currently in use. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cea9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cea9-106">Syntax</span></span>

<span data-ttu-id="9cea9-107">*expresión* . Versión</span><span class="sxs-lookup"><span data-stu-id="9cea9-107">*expression* .Version</span></span>

<span data-ttu-id="9cea9-108">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="9cea9-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cea9-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9cea9-109">Remarks</span></span>

<span data-ttu-id="9cea9-p102">El valor devuelto es un tipo de datos String que se evalúa en un número de versión en el formato "major.minor". Por ejemplo, "3.0". El número de versión del producto consta del número de versión (3), un punto y el número de lanzamiento (0).</span><span class="sxs-lookup"><span data-stu-id="9cea9-p102">The return value is a String that evaluates to a version number in the form "major.minor". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>


---
title: Propiedad DBEngine. DefaultType (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294382"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="f3b9d-102">Propiedad DBEngine. DefaultType (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3b9d-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="f3b9d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3b9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3b9d-104">Establece o devuelve un valor que indica qué tipo de área de trabajo se utilizará en el siguiente objeto **[Workspace](workspace-object-dao.md)** que se cree.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b9d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b9d-105">Syntax</span></span>

<span data-ttu-id="f3b9d-106">*expresión* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="f3b9d-106">*expression* .DefaultType</span></span>

<span data-ttu-id="f3b9d-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="f3b9d-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b9d-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3b9d-108">Remarks</span></span>

<span data-ttu-id="f3b9d-109">La configuración o el valor devuelto puede ser una de las constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="f3b9d-p101">[!NOTA] Las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Utilice ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f3b9d-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="f3b9d-112">La configuración se puede invalidar para un único objeto **Workspace** estableciendo el argumento Type en el método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f3b9d-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>


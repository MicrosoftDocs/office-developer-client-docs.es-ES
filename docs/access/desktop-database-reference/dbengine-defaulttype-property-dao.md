---
title: Propiedad DBEngine.DefaultType (DAO)
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
ms.openlocfilehash: ec8dbc1e758b19c15c1a08b9936fa3c00acabde6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925663"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="9c73b-102">Propiedad DBEngine.DefaultType (DAO)</span><span class="sxs-lookup"><span data-stu-id="9c73b-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="9c73b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c73b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c73b-104">Establece o devuelve un valor que indica qué tipo de área de trabajo se utilizará en el siguiente objeto **[Workspace](workspace-object-dao.md)** que se cree.</span><span class="sxs-lookup"><span data-stu-id="9c73b-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c73b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c73b-105">Syntax</span></span>

<span data-ttu-id="9c73b-106">*expresión* . DefaultType</span><span class="sxs-lookup"><span data-stu-id="9c73b-106">*expression* .DefaultType</span></span>

<span data-ttu-id="9c73b-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="9c73b-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c73b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c73b-108">Remarks</span></span>

<span data-ttu-id="9c73b-109">La configuración o el valor devuelto puede ser una de las constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9c73b-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="9c73b-p101">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9c73b-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="9c73b-112">El valor se puede invalidar para un único **Workspace** estableciendo el argumento type en el método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9c73b-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>


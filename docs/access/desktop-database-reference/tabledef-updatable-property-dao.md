---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4908699aaea69a001a1abd3761b78607ae2640a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869823"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="0eeeb-102">TableDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0eeeb-102">TableDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="0eeeb-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0eeeb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0eeeb-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eeeb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0eeeb-106">Syntax</span></span>

<span data-ttu-id="0eeeb-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="0eeeb-107">*expression* .Updatable</span></span>

<span data-ttu-id="0eeeb-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="0eeeb-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eeeb-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0eeeb-109">Remarks</span></span>

<span data-ttu-id="0eeeb-p102">El valor de la propiedad **Updatable** siempre es **True** para un nuevo objeto **TableDef** creado y **False** para un objeto **TableDef** vinculado. Un objeto **TableDef** nuevo sólo se puede anexar a una base de datos para la que el usuario actual tenga permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="0eeeb-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>


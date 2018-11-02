---
title: Propiedad TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 71202203588182ba2bf1ba1449f2b1ee04c82c67
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926202"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="6ac0b-102">Propiedad TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="6ac0b-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="6ac0b-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ac0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6ac0b-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="6ac0b-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac0b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ac0b-106">Syntax</span></span>

<span data-ttu-id="6ac0b-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="6ac0b-107">*expression* .Updatable</span></span>

<span data-ttu-id="6ac0b-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="6ac0b-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac0b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ac0b-109">Remarks</span></span>

<span data-ttu-id="6ac0b-p102">El valor de la propiedad **Updatable** siempre es **True** para un nuevo objeto **TableDef** creado y **False** para un objeto **TableDef** vinculado. Un objeto **TableDef** nuevo sólo se puede anexar a una base de datos para la que el usuario actual tenga permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="6ac0b-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>


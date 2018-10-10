---
title: TableDef.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44f24e68b60f69304a167d2b9b5ce0b4b0e69b11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486666"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="591ac-102">TableDef.Updatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="591ac-102">TableDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="591ac-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="591ac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="591ac-p101">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO. **Boolean** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="591ac-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="591ac-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="591ac-106">Syntax</span></span>

<span data-ttu-id="591ac-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="591ac-107">*expression* .Updatable</span></span>

<span data-ttu-id="591ac-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="591ac-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="591ac-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="591ac-109">Remarks</span></span>

<span data-ttu-id="591ac-p102">El valor de la propiedad **Updatable** siempre es **True** para un nuevo objeto **TableDef** creado y **False** para un objeto **TableDef** vinculado. Un objeto **TableDef** nuevo sólo se puede anexar a una base de datos para la que el usuario actual tenga permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="591ac-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>


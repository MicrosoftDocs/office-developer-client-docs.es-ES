---
title: Propiedad TableDef.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314416"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="f1a91-102">Propiedad TableDef.Updatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1a91-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="f1a91-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1a91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1a91-104">Devuelve un valor que indica si el usuario puede cambiar un objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="f1a91-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="f1a91-105">**Booleano** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f1a91-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a91-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1a91-106">Syntax</span></span>

<span data-ttu-id="f1a91-107">*expresión* . Actualizable</span><span class="sxs-lookup"><span data-stu-id="f1a91-107">*expression* .Updatable</span></span>

<span data-ttu-id="f1a91-108">*expression* Variable que representa un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="f1a91-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a91-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1a91-109">Remarks</span></span>

<span data-ttu-id="f1a91-p102">El valor de la propiedad **Updatable** siempre es **True** para un nuevo objeto **TableDef** creado y **False** para un objeto **TableDef** vinculado. Un objeto **TableDef** nuevo sólo se puede anexar a una base de datos para la que el usuario actual tenga permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="f1a91-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>


---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Determina si los usuarios especificados son amigos.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412565"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="ea87c-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="ea87c-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="ea87c-104">Determina si los usuarios especificados son amigos.</span><span class="sxs-lookup"><span data-stu-id="ea87c-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="ea87c-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="ea87c-105">Parameters</span></span>

<span data-ttu-id="ea87c-106">_userIds_</span><span class="sxs-lookup"><span data-stu-id="ea87c-106">_userIds_</span></span>
  
> <span data-ttu-id="ea87c-107">a Estructura que especifica una matriz de valores de identificador de usuario que corresponden a un conjunto de personas en la red social.</span><span class="sxs-lookup"><span data-stu-id="ea87c-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="ea87c-108">_obtener_</span><span class="sxs-lookup"><span data-stu-id="ea87c-108">_results_</span></span>
  
> <span data-ttu-id="ea87c-109">contempla Puntero a estructura que especifica una matriz de valores booleanos, que indica si la persona correspondiente de __ la matriz de identificadores de usuario es un amigo.</span><span class="sxs-lookup"><span data-stu-id="ea87c-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ea87c-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ea87c-110">Remarks</span></span>

<span data-ttu-id="ea87c-111">Para cada persona representada en la matriz de __ entrada del parámetro userids, este método establece el elemento correspondiente en la matriz de salida del parámetro _Results_ .</span><span class="sxs-lookup"><span data-stu-id="ea87c-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="ea87c-112">**true** indica que la persona es un amigo y **false** indica que la persona no es una amiga.</span><span class="sxs-lookup"><span data-stu-id="ea87c-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ea87c-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="ea87c-113">See also</span></span>

- [<span data-ttu-id="ea87c-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="ea87c-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)


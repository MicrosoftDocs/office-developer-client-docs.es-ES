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
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821099"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="e835e-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="e835e-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="e835e-104">Determina si los usuarios especificados son amigos.</span><span class="sxs-lookup"><span data-stu-id="e835e-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="e835e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e835e-105">Parameters</span></span>

<span data-ttu-id="e835e-106">_identificadores de usuario_</span><span class="sxs-lookup"><span data-stu-id="e835e-106">_userIds_</span></span>
  
> <span data-ttu-id="e835e-107">[entrada] Una estructura que especifica una matriz de valores de identificador de usuario que corresponden a un conjunto de personas en la red social.</span><span class="sxs-lookup"><span data-stu-id="e835e-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="e835e-108">_resultados_</span><span class="sxs-lookup"><span data-stu-id="e835e-108">_results_</span></span>
  
> <span data-ttu-id="e835e-109">[out] Un puntero a la estructura que especifica una matriz de valores booleanos, que indica si la persona correspondiente en la matriz de _identificadores de usuario_ es un amigo.</span><span class="sxs-lookup"><span data-stu-id="e835e-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e835e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e835e-110">Remarks</span></span>

<span data-ttu-id="e835e-111">Para cada persona representada en la matriz de entrada del parámetro de _identificadores de usuario_ , este método establece el elemento correspondiente en la matriz de salida del parámetro de _resultados_ .</span><span class="sxs-lookup"><span data-stu-id="e835e-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="e835e-112">**true** indica que la persona es un amigo y **false** indica que la persona no es un amigo.</span><span class="sxs-lookup"><span data-stu-id="e835e-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e835e-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="e835e-113">See also</span></span>

- [<span data-ttu-id="e835e-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="e835e-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)


---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtiene un valor de tipo string que representa a una o más personas que coinciden con el parámetro userID.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821114"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="6c054-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="6c054-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="6c054-104">Obtiene un valor de tipo string que representa a una o más personas que coinciden con el parámetro _userID_ .</span><span class="sxs-lookup"><span data-stu-id="6c054-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="6c054-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c054-105">Parameters</span></span>

<span data-ttu-id="6c054-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="6c054-106">_userId_</span></span>
  
> <span data-ttu-id="6c054-107">[entrada] Un identificador de usuario de redes sociales, dirección SMTP o nombre para mostrar de una persona.</span><span class="sxs-lookup"><span data-stu-id="6c054-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="6c054-108">_resultado_</span><span class="sxs-lookup"><span data-stu-id="6c054-108">_result_</span></span>
  
> <span data-ttu-id="6c054-109">[out] Una cadena XML que representa a una o más personas que coinciden con la información de identificación especificada por el parámetro _userId_ .</span><span class="sxs-lookup"><span data-stu-id="6c054-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6c054-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6c054-110">Remarks</span></span>

<span data-ttu-id="6c054-111">Si una o más personas coincide con la solicitud de **FindPerson** , este método devuelve la información de las personas en el parámetro de _resultado_ .</span><span class="sxs-lookup"><span data-stu-id="6c054-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="6c054-112">La cadena de _resultado_ XML debe cumplir con la definición del esquema para **amigos**, tal como se define en el esquema para la extensibilidad de proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="6c054-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c054-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c054-113">See also</span></span>

- [<span data-ttu-id="6c054-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c054-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)


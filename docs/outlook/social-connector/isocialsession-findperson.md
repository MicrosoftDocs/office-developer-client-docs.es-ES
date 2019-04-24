---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtiene una cadena que representa una o varias personas que coinciden con el parámetro userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285374"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="bf6c8-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="bf6c8-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="bf6c8-104">Obtiene una cadena que representa una o varias personas que coinciden con el parámetro _userid_ .</span><span class="sxs-lookup"><span data-stu-id="bf6c8-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="bf6c8-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="bf6c8-105">Parameters</span></span>

<span data-ttu-id="bf6c8-106">_Identificado_</span><span class="sxs-lookup"><span data-stu-id="bf6c8-106">_userId_</span></span>
  
> <span data-ttu-id="bf6c8-107">a Un identificador de usuario de red social, una dirección SMTP o el nombre para mostrar de una persona.</span><span class="sxs-lookup"><span data-stu-id="bf6c8-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="bf6c8-108">_result_</span><span class="sxs-lookup"><span data-stu-id="bf6c8-108">_result_</span></span>
  
> <span data-ttu-id="bf6c8-109">contempla Una cadena XML que representa una o varias personas que coinciden con la información de identificación especificada por el parámetro _userId_ .</span><span class="sxs-lookup"><span data-stu-id="bf6c8-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bf6c8-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf6c8-110">Remarks</span></span>

<span data-ttu-id="bf6c8-111">Si una o más personas coinciden con la solicitud **FindPerson** , este método devuelve la información de esas personas en el parámetro _result_ .</span><span class="sxs-lookup"><span data-stu-id="bf6c8-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="bf6c8-112">La cadena XML de _resultado_ debe cumplir con la definición de esquema para **amigos**, tal como se define en el esquema para la extensibilidad de proveedores de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="bf6c8-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf6c8-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf6c8-113">See also</span></span>

- [<span data-ttu-id="bf6c8-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bf6c8-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)


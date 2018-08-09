---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817296"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="a45d0-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="a45d0-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="a45d0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a45d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a45d0-105">Se basa en un icono de una de las propiedades del icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="a45d0-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="a45d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a45d0-106">Parameters</span></span>

 <span data-ttu-id="a45d0-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="a45d0-107">_nPropID_</span></span>
  
> <span data-ttu-id="a45d0-108">[entrada] Un identificador de propiedad para una propiedad de icono.</span><span class="sxs-lookup"><span data-stu-id="a45d0-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="a45d0-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="a45d0-109">_phicon_</span></span>
  
> <span data-ttu-id="a45d0-110">[out] Un puntero al icono devuelto.</span><span class="sxs-lookup"><span data-stu-id="a45d0-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a45d0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a45d0-111">Return value</span></span>

<span data-ttu-id="a45d0-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="a45d0-112">S_OK</span></span> 
  
> <span data-ttu-id="a45d0-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="a45d0-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a45d0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a45d0-114">Remarks</span></span>

<span data-ttu-id="a45d0-115">Las aplicaciones cliente de llaman al método **IMAPIFormInfo::MakeIconFromBinary** para crear un icono de una de las propiedades del icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="a45d0-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="a45d0-116">En el parámetro _nPropID_ , **MakeIconFromBinary** toma el identificador de propiedad de una de las propiedades del icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="a45d0-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="a45d0-117">Con este identificador de propiedad, que basa un icono que se puede mostrar en las vistas de tabla que incluyen columnas de propiedad para los iconos.</span><span class="sxs-lookup"><span data-stu-id="a45d0-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a45d0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a45d0-118">See also</span></span>



[<span data-ttu-id="a45d0-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a45d0-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


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
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405117"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="4192d-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="4192d-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="4192d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4192d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4192d-105">Crea un icono a partir de una de las propiedades de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="4192d-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="4192d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4192d-106">Parameters</span></span>

 <span data-ttu-id="4192d-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="4192d-107">_nPropID_</span></span>
  
> <span data-ttu-id="4192d-108">[in] Identificador de propiedad de una propiedad icon.</span><span class="sxs-lookup"><span data-stu-id="4192d-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="4192d-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="4192d-109">_phicon_</span></span>
  
> <span data-ttu-id="4192d-110">[salida] Puntero al icono devuelto.</span><span class="sxs-lookup"><span data-stu-id="4192d-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4192d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4192d-111">Return value</span></span>

<span data-ttu-id="4192d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4192d-112">S_OK</span></span> 
  
> <span data-ttu-id="4192d-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4192d-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4192d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4192d-114">Remarks</span></span>

<span data-ttu-id="4192d-115">Las aplicaciones cliente llaman **al método IMAPIFormInfo::MakeIconFromBinary** para crear un icono a partir de una de las propiedades de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="4192d-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="4192d-116">En el  _parámetro nPropID,_ **MakeIconFromBinary** toma el identificador de propiedad de una de las propiedades de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="4192d-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="4192d-117">Con este identificador de propiedad, crea un icono que se puede mostrar en vistas de tabla que incluyen columnas de propiedades para iconos.</span><span class="sxs-lookup"><span data-stu-id="4192d-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4192d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4192d-118">See also</span></span>



[<span data-ttu-id="4192d-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4192d-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


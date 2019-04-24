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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342115"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="57465-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="57465-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="57465-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57465-105">Crea un icono a partir de una de las propiedades de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="57465-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="57465-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="57465-106">Parameters</span></span>

 <span data-ttu-id="57465-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="57465-107">_nPropID_</span></span>
  
> <span data-ttu-id="57465-108">a Un identificador de propiedad para una propiedad Icon.</span><span class="sxs-lookup"><span data-stu-id="57465-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="57465-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="57465-109">_phicon_</span></span>
  
> <span data-ttu-id="57465-110">contempla Puntero al icono devuelto.</span><span class="sxs-lookup"><span data-stu-id="57465-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="57465-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57465-111">Return value</span></span>

<span data-ttu-id="57465-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="57465-112">S_OK</span></span> 
  
> <span data-ttu-id="57465-113">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="57465-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57465-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57465-114">Remarks</span></span>

<span data-ttu-id="57465-115">Las aplicaciones cliente llaman al método **IMAPIFormInfo:: MakeIconFromBinary** para crear un icono a partir de una de las propiedades de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="57465-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="57465-116">En el parámetro _nPropID_ , **MakeIconFromBinary** toma el identificador de la propiedad de una de las propiedades de icono de un formulario.</span><span class="sxs-lookup"><span data-stu-id="57465-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="57465-117">Mediante el uso de este identificador de propiedad, se crea un icono que se puede mostrar en las vistas de tabla que incluyen columnas de propiedades para los iconos.</span><span class="sxs-lookup"><span data-stu-id="57465-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57465-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="57465-118">See also</span></span>



[<span data-ttu-id="57465-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="57465-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)


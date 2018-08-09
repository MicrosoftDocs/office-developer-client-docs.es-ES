---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtiene la cuenta siguiente en el enumerador.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816261"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Obtiene la cuenta siguiente en el enumerador.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parámetros

_ppUnk_
  
> [entrada] Un puntero a una interfaz **IUnknown** que el cliente puede consultar para obtener una interfaz [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|S_FALSE  <br/> |El enumerador ha llegado al final.  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz especificada por *ppunk* hereda de **IUnknown**. El cliente puede consultar esta interfaz (mediante **IUnknown:: QueryInterface**) para obtener un puntero a una interfaz **IOlkAccount** y obtener o establecer la información de esta cuenta. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)


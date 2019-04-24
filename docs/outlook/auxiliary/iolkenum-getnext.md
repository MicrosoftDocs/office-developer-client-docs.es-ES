---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtiene la siguiente cuenta del enumerador.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321899"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Obtiene la siguiente cuenta del enumerador.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parameters

_ppunk_
  
> a Un puntero a una interfaz **IUnknown** que el cliente puede consultar para obtener una interfaz [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|S_FALSE  <br/> |El enumerador ha alcanzado el final.  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz especificada por *ppunk* hereda de **IUnknown**. El cliente puede consultar esta interfaz (mediante **IUnknown:: QueryInterface**) para obtener un puntero a una interfaz **IOlkAccount** y obtener o establecer información de esta cuenta. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)


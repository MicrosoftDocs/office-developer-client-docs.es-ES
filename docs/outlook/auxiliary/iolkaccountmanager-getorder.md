---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtiene el orden de la categoría de cuentas especificada.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424626"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

Obtiene el orden de la categoría de cuentas especificada.
  
## <a name="quick-info"></a>Información rápida

Consulta [IOlkAccountManager](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>Parámetros

_pclsidCategory_
  
> [entrada] Identificador de clase de categoría para el que se va a obtener el pedido. El valor debe ser uno de estos procedimientos:
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [salida] El número de cuentas. 
    
_prgAccts_
  
> [salida] Puntero a una matriz de cuentas.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada se ha realiza correctamente  <br/> |
|E_INVALIDARG  <br/> |Uno o más argumentos no son válidos.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |No se ha inicializado el Administrador de cuentas para su uso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Antes de llamar a este método, el llamador asigna solo un puntero de matriz *prgAccts,* pero no memoria para la matriz a la que *apunta prgAccts.* Después de que este método devuelve, el llamador debe usar [IOlkAccountManager::FreeMemory para](iolkaccountmanager-freememory.md) liberar la memoria asignada para  *prgAccts*  . 
  
## <a name="see-also"></a>Consulte también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)


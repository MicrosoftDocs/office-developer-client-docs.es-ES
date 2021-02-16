---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432838"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona una forma alternativa de invocar el método OLE **IUnknown::AddRef**. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Parámetros

 _tordo_
  
> [entrada] Puntero a una interfaz derivada de la **interfaz IUnknown,** es decir, cualquier interfaz MAPI. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen inesperado o desconocido impidió que se completara la operación.
    
## <a name="remarks"></a>Comentarios

 **UlAddRef devuelve** el valor devuelto por el método **IUnknown::AddRef,** que es el nuevo valor del recuento de referencias para la interfaz. El valor es distinto de cero. 
  
Para obtener más información **acerca de IUnknown::AddRef**, vea [Implementar la interfaz IUnknown](implementing-the-iunknown-interface.md). 
  


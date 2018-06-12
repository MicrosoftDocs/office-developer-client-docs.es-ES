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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: fc6c12d914e581c3f975e94809f0bdea73020099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820900"
---
# <a name="uladdref"></a>UlAddRef

  
  
**Se aplica a**: Outlook 
  
Proporciona una manera alternativa para invocar el método OLE **IUnknown:: AddRef**. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>Sintaxis

 _pUnk_
  
> [entrada] Puntero a una interfaz derivada de la interfaz **IUnknown** , en otras palabras cualquier interfaz MAPI. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen desconocido o inesperado no puede completar la operación.
    
## <a name="remarks"></a>Notas

 **UlAddRef** devuelve el valor devuelto por el método **IUnknown:: AddRef** , que es el nuevo valor del recuento de referencias para la interfaz. El valor es distinto de cero. 
  
Para obtener más información acerca de **IUnknown:: AddRef**, vea [implementación de la interfaz IUnknown](implementing-the-iunknown-interface.md). 
  


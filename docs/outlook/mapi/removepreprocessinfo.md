---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432950"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Quita de un mensaje la información preprocesada escrita por una función basada en [PreprocessMessage.](preprocessmessage.md) 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Función definida implementada por:  <br/> |Proveedores de transporte  <br/> |
|Función definida llamada por:  <br/> |Cola MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parámetros

 _lpMessage_
  
> [entrada] Puntero al mensaje preprocesado del que se va a quitar la información.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La información preprocesada se quitó correctamente.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama a una función basada en **RemovePreprocessInfo**. Un proveedor de transporte registra la función basada **en RemovePreprocessInfo** al mismo tiempo que registra la función basada **en PreprocessMessage** paralela en una llamada al método [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md) 
  
Una representación de imagen adecuada para la transmisión de fax es un ejemplo de información preprocesada escrita por una función definida por el prototipo de función [PreprocessMessage.](preprocessmessage.md) La cola MAPI normalmente llama a una **función RemovePreprocessInfo** después de enviar un mensaje que contiene información preprocesada. 
  


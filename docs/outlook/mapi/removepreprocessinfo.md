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
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588835"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Quita preprocesa escrita por una función [PreprocessMessage](preprocessmessage.md) en función de un mensaje de información. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapispi.h  <br/> |
|Función definido implementada por:  <br/> |Proveedores de transporte  <br/> |
|Llamado por una función definida:  <br/> |Cola MAPI  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>Parámetros

 _lpMessage_
  
> [entrada] Puntero al mensaje preprocesado desde la que es información que se va a quitar.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Información preprocesado se quitó correctamente.
    
## <a name="remarks"></a>Comentarios

La cola MAPI llama a una función según **RemovePreprocessInfo**. Un proveedor de transporte registra la función **RemovePreprocessInfo** en función al mismo tiempo que registra la función **PreprocessMessage** basado paralela en una llamada al método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) . 
  
Una imagen de representación adecuada para la transmisión de fax es un ejemplo de información preprocesado escrita por una función definida por el prototipo de función [PreprocessMessage](preprocessmessage.md). La cola MAPI normalmente llama a una función de **RemovePreprocessInfo** después de enviar un mensaje que contiene información preprocesado. 
  


---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404900"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Registra la función de preprocesador de un proveedor de transporte (una función que se ajusta al prototipo [PreprocessMessage).](preprocessmessage.md) 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpMuid_
  
> [entrada] Puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador que controla la función de preprocesador. El  _parámetro lpMuid_ puede ser NULL. 
    
 _lpszAdrType_
  
> [entrada] Puntero al tipo de dirección de los mensajes en los que opera la función, como FAX, SMTP o X500. El  _parámetro lpszAdrType_ puede ser NULL. 
    
 _lpszDLLName_
  
> [entrada] Puntero al nombre de la biblioteca de vínculos dinámicos (DLL) que contiene el punto de entrada de la función de preprocesador.
    
 _lpszPreprocess_
  
> [entrada] Puntero al nombre de la función de preprocesador. El  _parámetro lpszPreprocess_ puede ser NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [entrada] Puntero al nombre de la función que quita la información del preprocesador (una función que se ajusta al prototipo [RemovePreprocessInfo).](removepreprocessinfo.md) El  _parámetro lpszRemovePreprocessInfo_ puede ser NULL. 
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La función de preprocesador se registró correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::RegisterPreprocessor** se implementa únicamente para objetos de compatibilidad del proveedor de transporte. Los proveedores de transporte llaman a **RegisterPreprocessor** para registrar una función de preprocesador (una función que se ajusta al prototipo [PreprocessMessage).](preprocessmessage.md) Se debe registrar una función de preprocesador para que la cola MAPI pueda llamarla. 
  
Los parámetros  _lpszPreprocess_,  _lpszRemovePreprocessInfo_ y  _lpszDLLName_ deben apuntar a cadenas que se pueden usar junto con llamadas a la función **GetProcAddress** de Win32, lo que permite llamar correctamente al punto de entrada dll del preprocesador. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Las llamadas a preprocesadores son específicas del orden del proveedor de transporte. Esto significa que si otro proveedor de transporte anterior a su proveedor es capaz de controlar un mensaje, no se llamará a la función de preprocesador para ese mensaje. Solo se llamará a la función de preprocesador para los mensajes que controlará.
  
Puede escribir funciones de preprocesador para controlar un identificador específico almacenado en una estructura [MAPIUID](mapiuid.md) o un tipo de dirección. Si especifica una estructura **MAPIUID** en el parámetro  _lpMuid_ y un tipo de dirección en el parámetro  _lpszAdrType,_ se llamará a la función para los destinatarios de mensajes que coincidan con **MAPIUID** o con el tipo de dirección. Si  _lpMuid_ es NULL y  _lpszAdrType_ no es NULL, solo se llamará a la función para los destinatarios que tengan una dirección que coincida con el tipo al que apunta  _lpszAdrType_. Si  _lpMuid_ no es NULL y  _lpszAdrType_ es NULL, se llamará a la función para los destinatarios que coincidan con **MAPIUID,** independientemente de su tipo de dirección. Si ambos son NULL, se llama a la función para todos los destinatarios del mensaje.
  
## <a name="see-also"></a>Consulte también



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


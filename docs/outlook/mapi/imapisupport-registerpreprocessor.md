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
ms.openlocfilehash: 219c15fc00490983e970e4533f927cf4d91916b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817543"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Hace referencia a**: Outlook 
  
Registra la función de preprocesador del proveedor de transporte (una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ). 
  
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
  
> [entrada] Un puntero a la estructura [MAPIUID](mapiuid.md) que contiene el identificador que controla la función del preprocesador. El parámetro _lpMuid_ puede ser NULL. 
    
 _lpszAdrType_
  
> [entrada] Un puntero para el tipo de dirección para los mensajes de la función opera en, como FAX, SMTP o X500. El parámetro _lpszAdrType_ puede ser NULL. 
    
 _lpszDLLName_
  
> [entrada] Un puntero en el nombre de la biblioteca de vínculos dinámicos (DLL) que contiene el punto de entrada para la función de preprocesador.
    
 _lpszPreprocess_
  
> [entrada] Un puntero en el nombre de la función del preprocesador. El parámetro _lpszPreprocess_ puede ser NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [entrada] Un puntero en el nombre de la función que quita la información del preprocesador (una función que se ajusta al prototipo [RemovePreprocessInfo](removepreprocessinfo.md) ). El parámetro _lpszRemovePreprocessInfo_ puede ser NULL. 
    
 _ulFlags_
  
> Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La función del preprocesador se ha registrado correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::RegisterPreprocessor** se implementa para los objetos de soporte técnico de proveedor de transporte sólo. Los proveedores de transporte llame a **RegisterPreprocessor** para registrar una función del preprocesador (es decir, una función que se ajusta al prototipo [PreprocessMessage](preprocessmessage.md) ). Una función del preprocesador debe estar registrada antes de la cola MAPI puede llamarlo. 
  
Los parámetros _lpszPreprocess_, _lpszRemovePreprocessInfo_y _lpszDLLName_ deben apuntar a las cadenas que se pueden usar en combinación con llamadas a la función de Win32 **GetProcAddress** , lo que permite DLL del preprocesador punto de entrada que se llama correctamente. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Las llamadas a preprocessors son específicas de orden del proveedor de transporte. Esto significa que, si otro proveedor de transporte por delante de su proveedor es capaz de controlar un mensaje, no se llamará su función preprocesador para ese mensaje. Se llamará a la función del preprocesador únicamente para los mensajes que va a controlar.
  
Puede escribir funciones del preprocesador para controlar un identificador de específico almacenado en una estructura [MAPIUID](mapiuid.md) o un tipo de dirección. Si especifica ambos una estructura **MAPIUID** en el parámetro _lpMuid_ y un tipo de dirección en el parámetro _lpszAdrType_ , la función se llamará para los destinatarios del mensaje que coinciden con el **MAPIUID** o el tipo de dirección. Si _lpMuid_ es NULL y _lpszAdrType_ no es NULL, la función se llamará sólo para los destinatarios que tienen una dirección que coincide con el tipo que señala _lpszAdrType_. Si _lpMuid_ es no nulo y _lpszAdrType_ es NULL, la función se llamará para los destinatarios que coinciden con **MAPIUID**, independientemente de su tipo de dirección. Si ambos son NULL, la función se llama para todos los destinatarios del mensaje.
  
## <a name="see-also"></a>Vea también



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


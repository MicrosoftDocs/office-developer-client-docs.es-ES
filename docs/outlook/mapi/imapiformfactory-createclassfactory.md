---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817301"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Se aplica a**: Outlook 
  
Devuelve un objeto de fábrica de clase para el formulario.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Sintaxis

 _clsidForm_
  
> [entrada] Un identificador de clase para el formulario que se creará la fábrica de clase.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppClassFactory_
  
> [out] Un puntero al objeto de fábrica de clase.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se devuelve el objeto de fábrica de clase.
    
## <a name="remarks"></a>Notas

Visores de formulario llamar al método **IMAPIFormFactory::CreateClassFactory** para obtener un generador de clases para un formulario específico. La fábrica de clase se usa para crear instancias de un formulario que controla los mensajes de una clase específica y para controlar el acceso a estas instancias. 
  
Se llama al método de **CreateClassFactory** por los visores de formulario para obtener un objeto de fábrica de clase para los servidores de formulario que implementan varias clases de mensaje. Este método recibe un identificador de clase (CLSID) como un parámetro. En función de dicho parámetro, este método puede determinar el tipo específico del objeto de fábrica de clase que se va a devolver. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede devolver desde la implementación de **CreateClassFactory** el mismo objeto de fábrica de clase en varias llamadas para el mismo identificador de clase. Creación de una nueva instancia de la fábrica de clase no es necesario. 
  
Puede tener una implementación de fábrica de clase único que crea instancias de la fábrica de clase adecuada a petición o varias implementaciones de fábrica de clase, uno para cada clase de mensaje.
  
## <a name="see-also"></a>Ver también



[IMAPIFormFactory: IUnknown](imapiformfactoryiunknown.md)


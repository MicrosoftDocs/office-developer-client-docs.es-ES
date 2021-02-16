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
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416079"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un objeto de fábrica de clase para el formulario.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parámetros

 _clsidForm_
  
> [entrada] Identificador de clase para el formulario que va a crear la fábrica de clases.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppClassFactory_
  
> [salida] Puntero al objeto de fábrica de clase.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha devuelto el objeto de fábrica de clase.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al **método IMAPIFormFactory::CreateClassFactory** para obtener una fábrica de clases para un formulario específico. La fábrica de clases se usa para crear instancias de un formulario que controla los mensajes de una clase específica y para controlar el acceso a estas instancias. 
  
Los visores de formularios llaman al método **CreateClassFactory** para obtener un objeto de fábrica de clase para servidores de formulario que implementan varias clases de mensajes. Este método recibe un identificador de clase (CLSID) como parámetro. En función de ese parámetro, este método puede determinar el tipo específico de objeto de fábrica de clase que se va a devolver. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede devolver de la implementación **CreateClassFactory** el mismo objeto de fábrica de clase en varias llamadas para el mismo identificador de clase. No es necesario crear una nueva instancia de fábrica de clase. 
  
Puedes tener una implementación de fábrica de una sola clase que cree instancias de fábrica de clase adecuadas a petición, o varias implementaciones de fábrica de clases, una para cada clase de mensaje.
  
## <a name="see-also"></a>Consulte también



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


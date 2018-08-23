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
ms.openlocfilehash: cb5cb5a0169e716f7fcc7f596660bc0222c51c84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572161"
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
  
> [entrada] Un identificador de clase para el formulario que se creará la fábrica de clase.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppClassFactory_
  
> [out] Un puntero al objeto de fábrica de clase.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se devuelve el objeto de fábrica de clase.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IMAPIFormFactory::CreateClassFactory** para obtener un generador de clases para un formulario específico. La fábrica de clase se usa para crear instancias de un formulario que controla los mensajes de una clase específica y para controlar el acceso a estas instancias. 
  
Se llama al método de **CreateClassFactory** por los visores de formulario para obtener un objeto de fábrica de clase para los servidores de formulario que implementan varias clases de mensaje. Este método recibe un identificador de clase (CLSID) como un parámetro. En función de dicho parámetro, este método puede determinar el tipo específico del objeto de fábrica de clase que se va a devolver. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Puede devolver desde la implementación de **CreateClassFactory** el mismo objeto de fábrica de clase en varias llamadas para el mismo identificador de clase. Creación de una nueva instancia de la fábrica de clase no es necesario. 
  
Puede tener una implementación de fábrica de clase único que crea instancias de la fábrica de clase adecuada a petición o varias implementaciones de fábrica de clase, uno para cada clase de mensaje.
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


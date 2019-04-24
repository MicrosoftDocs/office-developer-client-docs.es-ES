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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342178"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve un objeto de generador de clases para el formulario.
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>Parameters

 _clsidForm_
  
> a Identificador de clase para el formulario que el generador de clases va a crear.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lppClassFactory_
  
> contempla Un puntero al objeto generador de clases.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se devolvió el objeto de generador de clases.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IMAPIFormFactory:: CreateClassFactory** para obtener un generador de clases para un formulario específico. El generador de clases se usa para crear instancias de un formulario que controla mensajes de una clase específica y para controlar el acceso a estas instancias. 
  
Los visores de formulario llaman al método **CreateClassFactory** para obtener un objeto de generador de clases para servidores de formularios que implementen varias clases de mensajes. Este método recibe un identificador de clase (CLSID) como parámetro. Basándose en ese parámetro, este método puede determinar el tipo específico de objeto de generador de clase que se va a devolver. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Puede volver de la implementación de **CreateClassFactory** el mismo objeto de generador de clases en varias llamadas para el mismo identificador de clase. No es necesario crear una nueva instancia de generador de clases. 
  
Puede tener una implementación de fábrica de clase única que cree las instancias de fábrica de clases apropiadas a petición o varias implementaciones de fábrica de clases, una para cada clase de mensaje.
  
## <a name="see-also"></a>Vea también



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


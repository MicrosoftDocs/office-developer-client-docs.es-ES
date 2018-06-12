---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2d37898b100398218d4f8762cdd3a16943d8f11a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817980"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Se aplica a**: Outlook 
  
Permite que el proveedor de servicios de llamada o la puerta de enlace Agregar propiedades a la encapsulación de un mensaje o datos adjuntos. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo se incluyen o excluyen de encapsulación propiedades. Se pueden establecer los siguientes indicadores:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codifica sólo las propiedades en el parámetro _lpPropList_ que forman parte de los datos adjuntos en el mensaje. 
    
TNEF_PROP_CONTAINED 
  
> Codifica sólo las propiedades de los datos adjuntos especificados por el parámetro _ulElemID_ . Si el parámetro _lpvData_ no es nulo, se escriben los datos que apunta en encapsulación de los datos adjuntos en el archivo indicado por la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codifica sólo las propiedades desde el mensaje o adjunto especificado por el parámetro _ulElemID_ . Si se establece este indicador, el valor de _lpvData_ debe ser un puntero de [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) . 
    
TNEF_PROP_EXCLUDE 
  
> Codifica todas las propiedades que no se especifica en el parámetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Codifica todas las propiedades especificadas en _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codifica sólo las propiedades especificadas en _lpPropList_ que forman parte del propio mensaje. 
    
 _ulElemID_
  
> [entrada] Propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de un documento adjunto, que contiene un número que identifica de forma exclusiva identifica los datos adjuntos en el mensaje de su elemento primario. El parámetro _ulElemID_ se usa cuando se solicita un tratamiento especial para los datos adjuntos. El parámetro _ulElemID_ debe ser 0, a menos que se establece la marca TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF en el parámetro _ulFlags_ . 
    
 _lpvData_
  
> [entrada] Un puntero a datos adjuntos que usar para reemplazar los datos de los datos adjuntos especificados en _ulElemID_. El parámetro _lpvData_ debe ser NULL a menos que TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF está establecida en _ulFlags_.
    
 _lpPropList_
  
> [entrada] Un puntero a la lista de propiedades para incluir o excluir de encapsulación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::AddProps** a las propiedades de lista para que se incluyan o excluyan del procesamiento de formato de encapsulación neutro para el transporte (TNEF) de un mensaje o un archivo adjunto. Mediante llamadas sucesivas, el proveedor o la puerta de enlace puede especificar una lista de propiedades para agregar y codificar o para impedir que se codifica. Los proveedores y las puertas de enlace también pueden usar **AddProps** para proporcionar deben proporcionar información sobre cualquier tratamiento especial de los datos adjuntos. 
  
 **AddProps** sólo se admite para objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx](opentnefstreamex.md) . 
  
Tenga en cuenta que no hay codificación TNEF real ocurre para **AddProps** hasta que se llama al método [ITnef::Finish](itnef-finish.md) . Esta funcionalidad significa que punteros pasados a **AddProps** deben permanecer válidos hasta después de que se realiza la llamada al **Finalizar** . En ese momento, todos los objetos y datos pasadas con las llamadas de **AddProps** pueden publicados o liberados. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa el método **ITnef::AddProps** para copiar las propiedades de un mensaje a una secuencia TNEF.  <br/> |
   
## <a name="see-also"></a>Ver también



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónico PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef: IUnknown](itnefiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)


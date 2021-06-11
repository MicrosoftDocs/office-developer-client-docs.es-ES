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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348625"
---
# <a name="itnefaddprops"></a>ITnef::AddProps

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite al proveedor de servicios de llamadas o puerta de enlace agregar propiedades a la encapsulación de un mensaje o datos adjuntos. 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se incluyen o excluyen las propiedades de la encapsulación. Se pueden establecer las siguientes marcas:
    
TNEF_PROP_ATTACHMENTS_ONLY 
  
> Codifica solo las propiedades del parámetro  _lpPropList_ que forman parte de los datos adjuntos del mensaje. 
    
TNEF_PROP_CONTAINED 
  
> Codifica solo las propiedades de los datos adjuntos especificados por _el parámetro ulElemID._ Si el parámetro  _lpvData_ no es NULL, los datos señalados se escriben en la encapsulación de los datos adjuntos en el archivo indicado por la propiedad **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).
    
TNEF_PROP_CONTAINED_TNEF 
  
> Codifica solo las propiedades del mensaje o los datos adjuntos especificados por _el parámetro ulElemID._ Si se establece esta marca, el valor de _lpvData_ debe ser un [puntero IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) 
    
TNEF_PROP_EXCLUDE 
  
> Codifica todas las propiedades no especificadas en el _parámetro lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Codifica todas las propiedades especificadas en  _lpPropList_. 
    
TNEF_PROP_MESSAGE_ONLY 
  
> Codifica solo las propiedades especificadas en  _lpPropList_ que forman parte del propio mensaje. 
    
 _ulElemID_
  
> [in] Propiedad de **PR_ATTACH_NUM** datos adjuntos ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), que contiene un número que identifica de forma única los datos adjuntos en su mensaje primario. El  _parámetro ulElemID_ se usa cuando se solicita un tratamiento especial para los datos adjuntos. El _parámetro ulElemID_ debe ser 0 a menos que la marca TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF esté establecida en _el parámetro ulFlags._ 
    
 _lpvData_
  
> [in] Puntero a datos adjuntos usados para reemplazar los datos de los datos adjuntos especificados en  _ulElemID_. El  _parámetro lpvData_ debe ser NULL a menos que TNEF_PROP_CONTAINED o TNEF_PROP_CONTAINED_TNEF se establezca en  _ulFlags_.
    
 _lpPropList_
  
> [in] Puntero a la lista de propiedades que se incluirán o excluirán de la encapsulación.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacén de mensajes y las puertas de enlace llaman al método **ITnef::AddProps** para enumerar las propiedades que se incluirán o excluirán del procesamiento de formato de encapsulación (TNEF) de Transport-Neutral de un mensaje o datos adjuntos. Al usar llamadas sucesivas, el proveedor o la puerta de enlace pueden especificar una lista de propiedades para agregar y codificar o excluir de la codificación. Los proveedores y puertas de enlace también pueden usar **AddProps** para proporcionar información sobre los datos adjuntos de control especiales que se deben proporcionar. 
  
 **AddProps** solo se admite para objetos TNEF que se abren con la marca TNEF_ENCODE para la función [OpenTnefStream](opentnefstream.md) o [OpenTnefStreamEx.](opentnefstreamex.md) 
  
Tenga en cuenta que no se produce ninguna codificación TNEF real para **AddProps** hasta que se llama al método [ITnef::Finish.](itnef-finish.md) Esta funcionalidad significa que los punteros pasados **a AddProps** deben seguir siendo válidos hasta después de realizar la llamada a **Finish.** En ese momento, todos los objetos y datos pasados con **llamadas AddProps** se pueden liberar o liberar. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI usa el **método ITnef::AddProps** para copiar propiedades de un mensaje en una secuencia TNEF.  <br/> |
   
## <a name="see-also"></a>Vea también



[ITnef::Finish](itnef-finish.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Propiedad canónica PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)


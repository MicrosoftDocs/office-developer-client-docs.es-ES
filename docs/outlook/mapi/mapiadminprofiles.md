---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357333"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un objeto de administración de perfiles. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> a Máscara de máscara de los indicadores que indican las opciones de la función de entrada de servicio. 
    
 _lppProfAdmin_
  
> contempla Puntero a un puntero al nuevo objeto de administración de perfiles.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: GetProfAdmin  <br/> |MFCMAPI usa el método **MAPIAdminProfiles** para obtener el objeto de administración de perfiles.  <br/> |
   
## <a name="see-also"></a>Vea también



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)


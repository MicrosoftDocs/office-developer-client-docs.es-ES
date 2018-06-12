---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Representa a una persona en la red social.
ms.openlocfilehash: d6fca18ac2d2074239bd8b435bcd40971de83670
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821104"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson: IUnknown

Representa a una persona en la red social.
  
## <a name="members"></a>Miembros

La siguiente tabla muestran a los miembros que están disponibles en la interfaz **ISocialPerson** . 
  
|**Name**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Método  <br/> |Este método ha quedado obsoleto desde Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Método  <br/> |Obtiene una cadena que representa los detalles de la persona, como el nombre, apellidos y una dirección URL a una imagen de perfil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Método  <br/> |Obtiene una cadena que representa una colección de personas.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Método  <br/> |Este método no se admite actualmente.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Método  <br/> |Obtiene una matriz de bytes que contiene el recurso de imagen para la persona.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Método  <br/> |Este método no se admite actualmente.  <br/> |
   
## <a name="remarks"></a>Notas

Un proveedor de Outlook Social Connector (OSC) debe implementar esta interfaz para comunicarse con el OSC.
  
## <a name="see-also"></a>Ver también

- [Interfaces del proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)


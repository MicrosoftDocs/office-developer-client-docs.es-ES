---
title: IUnknown ISocialPerson
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Representa una persona de la red social.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331944"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

Representa una persona de la red social.
  
## <a name="members"></a>Members

En la siguiente tabla se muestran los miembros que están disponibles en la interfaz **ISocialPerson** . 
  
|**Name**|**Tipo de miembro**|**Descripción**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Método  <br/> |Este método está en desuso desde Outlook Social Connector 2013.  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Método  <br/> |Obtiene una cadena que representa los detalles de la persona, como el nombre, el apellido y una dirección URL de una imagen de perfil.  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Método  <br/> |Obtiene una cadena que representa una colección de personas.  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Método  <br/> |Actualmente, este método no es compatible.  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Método  <br/> |Obtiene una matriz de bytes que contiene el recurso de imagen de la persona.  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Método  <br/> |Actualmente, este método no es compatible.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un proveedor de Outlook Social Connector (OSC) debe implementar esta interfaz para comunicarse con el OSC.
  
## <a name="see-also"></a>Vea también

- [Interfaces de proveedor de Outlook Social Connector](outlook-social-connector-provider-interfaces.md)


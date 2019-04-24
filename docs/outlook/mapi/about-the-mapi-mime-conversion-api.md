---
title: Información sobre la API de conversión de MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321822"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Información sobre la API de conversión de MAPI-MIME

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de conversión de MAPI-MIME permite a los proveedores de correo convertir entre objetos MIME y mensajes MAPI. Proporciona definiciones de constantes, identificadores de clase e identificadores de interfaz, tal y como se muestra en las [constantes MAPI](mapi-constants.md). Los proveedores de correo deben crear una instancia de **[IConverterSession](iconvertersessioniunknown.md)** llamando a la función **CoCreateInstance** . 
  


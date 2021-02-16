---
title: Información sobre la API de conversión de MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420440"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Información sobre la API de conversión de MAPI-MIME

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de conversión MAPI-MIME permite a los proveedores de correo convertir entre objetos MIME y mensajes MAPI. Proporciona definiciones de constantes, identificadores de clase e identificadores de interfaz, como se muestra en [las constantes MAPI](mapi-constants.md). Los proveedores de correo deben crear una instancia de **[IConverterSession](iconvertersessioniunknown.md)** llamando a la **función CoCreateInstance.** 
  


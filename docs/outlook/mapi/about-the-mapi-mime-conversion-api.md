---
title: Información sobre la API de conversión de MAPI-MIME
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575269"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Información sobre la API de conversión de MAPI-MIME

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de conversión de MIME a MAPI permite a los proveedores de correo convertir entre los mensajes MAPI y objetos MIME. Proporciona definiciones de constantes, los identificadores de clase y los identificadores de interfaz tal como se muestra en [Las constantes de MAPI](mapi-constants.md). Proveedores de correo deben cocreate una instancia de **[IConverterSession](iconvertersessioniunknown.md)** mediante una llamada a la función **CoCreateInstance** . 
  


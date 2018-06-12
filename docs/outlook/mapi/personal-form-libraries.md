---
title: Bibliotecas de formularios personales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818474"
---
# <a name="personal-form-libraries"></a>Bibliotecas de formularios personales

  
  
**Se aplica a**: Outlook 
  
Como su nombre sugiere, bibliotecas de formularios personales contienen formularios de interés para un usuario determinado. Biblioteca de formularios personal de un usuario es la biblioteca de formularios asociada con el almacén de mensajes predeterminado identificado en el perfil del usuario; cada perfil instalado en una estación de trabajo puede usar un almacén independiente predeterminada y, por lo tanto, una biblioteca de formularios personales independientes. Una biblioteca de formularios personal puede contener copias de los formularios que se incluyen también en otras bibliotecas de formularios, además de otras formas.
  
Una biblioteca de formularios personales se implementa en la tabla de contenido asociados de la carpeta raíz en el almacén de mensajes de un usuario de forma predeterminada, si reside en un servidor o localmente en la estación de trabajo del usuario es irrelevante. Si el almacén de mensajes predeterminado del usuario se almacena en la estación de trabajo del usuario, las bibliotecas de formularios personales ofrecen un rendimiento mejorado mediante la habilitación de aplicaciones tengan acceso a los formularios de forma local en lugar de a través de la red. También facilita formularios disponibles para los usuarios que trabajan sin conexión, que pueden producirse cuando los usuarios desean tomar sus formularios con ellos en equipos portátiles y son sin acceso a una red.
  
Las propiedades y la implementación subyacente de entradas de la biblioteca de formularios personal incluyen una propiedad de "Contenedor ID" que identifica un contenedor principal que debe sincronizarse con la entrada local. Esto puede ser el identificador de una carpeta arbitrario que contiene los formularios. Esto es útil si está utilizando el Administrador de un formulario personalizado que es compatible con algún tipo de biblioteca de formularios de toda la organización; el Administrador de formulario se ocupa de la sincronización de los formularios que se almacenan en la biblioteca de formularios personales y la biblioteca de formularios de toda la organización. Esto sucede probablemente cuando el Administrador de formulario se cargó, pero puede suceder en teoría en cualquier momento.
  
## <a name="see-also"></a>Ver también



[Formularios MAPI](mapi-forms.md)


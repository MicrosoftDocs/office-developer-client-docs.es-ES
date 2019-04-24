---
title: Bibliotecas de formularios personales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348450"
---
# <a name="personal-form-libraries"></a>Bibliotecas de formularios personales

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Como su nombre sugiere, las bibliotecas de formularios personales contienen formularios de interés para un usuario en particular. La biblioteca de formularios personal de un usuario es la biblioteca de formularios asociada con el almacén de mensajes predeterminado identificado en el perfil del usuario; cada perfil instalado en una estación de trabajo puede usar un almacén predeterminado independiente y, por lo tanto, una biblioteca de formularios personal independiente. Una biblioteca de formularios personal puede contener copias de formularios que también se encuentran en otras bibliotecas de formularios además de otros formularios.
  
Una biblioteca de formularios personal se implementa en la tabla de contenido asociado de la carpeta raíz en el almacén de mensajes predeterminado del usuario, ya que reside en un servidor o localmente en la estación de trabajo del usuario es irrelevante. Si el almacén de mensajes predeterminado del usuario se almacena en la estación de trabajo del usuario, las bibliotecas de formularios personales ofrecen un rendimiento mejorado al permitir que las aplicaciones obtengan acceso a los formularios de forma local en lugar de a través de la red. También pone los formularios a disposición de los usuarios que trabajan sin conexión, lo que puede ocurrir cuando los usuarios quieren llevar sus formularios con ellos en equipos portátiles y no tienen acceso a una red.
  
Las propiedades y la implementación subyacente de las entradas de la biblioteca de formularios personales incluyen una propiedad "Container ID" que identifica un contenedor maestro con el que se debe sincronizar la entrada local. Puede ser el identificador de una carpeta arbitraria que contiene formularios. Esto es útil si está usando un administrador de formularios personalizado que admite algún tipo de biblioteca de formularios para toda la organización; el administrador de formularios se ocupará de sincronizar los formularios almacenados en la biblioteca de formularios personal y en la biblioteca de formularios de toda la organización. Esto probablemente ocurrirá cuando se cargó el administrador de formularios, pero esto puede ocurrir teóricamente en cualquier momento.
  
## <a name="see-also"></a>Vea también



[Formularios MAPI](mapi-forms.md)


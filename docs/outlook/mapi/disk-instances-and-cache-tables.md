---
title: Instancias de disco y tablas de caché
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4f0b66476b1ab3d149b6f7e7b8171de7a509b597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338853"
---
# <a name="disk-instances-and-cache-tables"></a>Instancias de disco y tablas de caché

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para activar un formulario, sus archivos ejecutables deben estar disponibles en el equipo del usuario. Si no están disponibles, se deben copiar desde la biblioteca de formularios al disco local. Para ello, el administrador de formularios predeterminado crea un subdirectorio en el directorio de Windows del usuario para que contenga los archivos ejecutables del formulario (. Exe,. HLPs). Este directorio se conoce como la instancia de disco del formulario.
  
El administrador de formulario predeterminado mantiene una tabla de todas las instancias de disco, de modo que si ya existe una instancia de disco, se puede usar sin tener que copiar los archivos de la biblioteca de formularios en el disco del usuario. La tabla de instancias de disco se administra como una memoria caché de uso menos frecuente. Si se necesita una nueva instancia de disco, se copia en el equipo del usuario y reemplaza la instancia de disco que se usa menos frecuentemente. A continuación, se actualiza la tabla de caché de instancias de disco para reflejar la configuración más reciente. El tamaño de la caché de disco es una opción configurable por el usuario, lo que permite a los usuarios equilibrar la velocidad con la capacidad de disco disponible.
  
Además de la caché de la instancia de disco, el administrador de formulario predeterminado mantiene una tabla de instancia en ejecución que enumera todas las instancias de servidores de formulario en ejecución en el equipo del usuario. Esto usa la capacidad de MAPI para mantener las instancias de formulario inactivas ejecutándose en un estado invisible hasta que se activa un formulario de la clase de mensaje del servidor de formularios. Es decir, los servidores de formularios se pueden almacenar en la memoria caché para minimizar el número de veces que el ejecutable de un formulario debe encontrarse en una biblioteca de formularios y cargarse en la memoria desde el disco o a través de la red. Al igual que la memoria caché de la instancia de disco, la caché de la instancia en ejecución se comporta de forma menos frecuente, por lo que se puede purgar una instancia de formulario en ejecución de la memoria caché para dejar espacio para otra instancia de formulario. Esta caché se busca en una instancia en ejecución de un servidor de formularios antes de que se busque en las bibliotecas de formularios para el servidor de formularios.
  
> [!NOTE]
> El administrador de formularios predeterminado muestra un indicador de progreso cuando se instala un formulario en la estación de trabajo de un usuario, lo que permite al usuario cancelar la operación. Esto es especialmente útil si la conexión del usuario con el archivo ejecutable del servidor de formularios se encuentra en una red de ancho de banda bajo. 
  
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)


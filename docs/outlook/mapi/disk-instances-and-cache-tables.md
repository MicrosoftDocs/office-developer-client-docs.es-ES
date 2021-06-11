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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436758"
---
# <a name="disk-instances-and-cache-tables"></a>Instancias de disco y tablas de caché

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para activar un formulario, sus archivos ejecutables deben estar disponibles en el equipo del usuario. Si no están disponibles, deben copiarse desde la biblioteca de formularios al disco local. Para ello, el administrador de formularios predeterminado crea un subdirectorio en el directorio de Windows usuario para contener los archivos ejecutables del formulario (. EXEs,. HLP). Este directorio se conoce como la instancia de disco del formulario.
  
El administrador de formularios predeterminado mantiene una tabla de todas las instancias de disco para que, si ya existe una instancia de disco, se pueda usar sin tener que copiar archivos de la biblioteca de formularios en el disco del usuario. La tabla de instancias de disco se administra como una memoria caché de uso menos frecuente. Si se necesita una nueva instancia de disco, se copia en el equipo del usuario, reemplazando la instancia de disco que se usa con menos frecuencia. A continuación, se actualiza la tabla de caché de instancias de disco para reflejar la configuración más reciente. El tamaño de la memoria caché de disco es una opción configurable por el usuario, que permite a los usuarios equilibrar la velocidad con la capacidad de disco disponible.
  
Además de la memoria caché de instancias de disco, el administrador de formularios predeterminado mantiene una tabla de instancia en ejecución que enumera todas las instancias en ejecución de servidores de formulario en el equipo del usuario. Esto usa la capacidad de MAPI para mantener las instancias de formulario inactivas ejecutándose en un estado invisible hasta que se active un formulario de la clase de mensaje de ese servidor de formularios. En otras palabras, los servidores de formulario se pueden almacenar en caché en ram para minimizar el número de veces que el archivo ejecutable de un formulario debe estar ubicado dentro de una biblioteca de formularios y cargarse en la memoria desde el disco o a través de la red. Al igual que la memoria caché de instancias de disco, la memoria caché de instancia en ejecución se comporta de forma menos frecuente para que una instancia de formulario en ejecución se pueda purgar de la memoria caché para dar espacio a otra instancia de formulario. Se busca en esta memoria caché una instancia en ejecución de un servidor de formularios antes de buscar en las bibliotecas de formularios el servidor de formularios.
  
> [!NOTE]
> El administrador de formularios predeterminado muestra un indicador de progreso al instalar un formulario en la estación de trabajo de un usuario, lo que permite al usuario cancelar la operación. Esto es especialmente útil si la conexión del usuario con el archivo ejecutable del servidor de formulario se encuentra a través de una red de ancho de banda bajo. 
  
## <a name="see-also"></a>Vea también

- [Formularios MAPI](mapi-forms.md)


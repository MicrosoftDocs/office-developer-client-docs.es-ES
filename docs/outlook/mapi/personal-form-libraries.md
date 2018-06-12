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
# <a name="personal-form-libraries"></a><span data-ttu-id="99873-103">Bibliotecas de formularios personales</span><span class="sxs-lookup"><span data-stu-id="99873-103">Personal Form Libraries</span></span>

  
  
<span data-ttu-id="99873-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="99873-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="99873-105">Como su nombre sugiere, bibliotecas de formularios personales contienen formularios de interés para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="99873-105">As its name suggests, personal form libraries contain forms of interest to a particular user.</span></span> <span data-ttu-id="99873-106">Biblioteca de formularios personal de un usuario es la biblioteca de formularios asociada con el almacén de mensajes predeterminado identificado en el perfil del usuario; cada perfil instalado en una estación de trabajo puede usar un almacén independiente predeterminada y, por lo tanto, una biblioteca de formularios personales independientes.</span><span class="sxs-lookup"><span data-stu-id="99873-106">A user's personal form library is the form library associated with the default message store identified in the user's profile; each profile installed on a workstation can use a separate default store, and therefore, a separate personal form library.</span></span> <span data-ttu-id="99873-107">Una biblioteca de formularios personal puede contener copias de los formularios que se incluyen también en otras bibliotecas de formularios, además de otras formas.</span><span class="sxs-lookup"><span data-stu-id="99873-107">A personal form library can contain copies of forms that are also contained in other form libraries in addition to other forms.</span></span>
  
<span data-ttu-id="99873-108">Una biblioteca de formularios personales se implementa en la tabla de contenido asociados de la carpeta raíz en el almacén de mensajes de un usuario de forma predeterminada, si reside en un servidor o localmente en la estación de trabajo del usuario es irrelevante.</span><span class="sxs-lookup"><span data-stu-id="99873-108">A personal form library is implemented in the associated-contents table of the root folder in a user's default message store — whether that resides on a server or locally on the user's workstation is immaterial.</span></span> <span data-ttu-id="99873-109">Si el almacén de mensajes predeterminado del usuario se almacena en la estación de trabajo del usuario, las bibliotecas de formularios personales ofrecen un rendimiento mejorado mediante la habilitación de aplicaciones tengan acceso a los formularios de forma local en lugar de a través de la red.</span><span class="sxs-lookup"><span data-stu-id="99873-109">If the user's default message store is stored on the user's workstation, personal form libraries offer enhanced performance by enabling applications to access forms locally instead of over the network.</span></span> <span data-ttu-id="99873-110">También facilita formularios disponibles para los usuarios que trabajan sin conexión, que pueden producirse cuando los usuarios desean tomar sus formularios con ellos en equipos portátiles y son sin acceso a una red.</span><span class="sxs-lookup"><span data-stu-id="99873-110">It also makes forms available to users working offline, which can occur when users want to take their forms with them on portable computers and are without access to a network.</span></span>
  
<span data-ttu-id="99873-111">Las propiedades y la implementación subyacente de entradas de la biblioteca de formularios personal incluyen una propiedad de "Contenedor ID" que identifica un contenedor principal que debe sincronizarse con la entrada local.</span><span class="sxs-lookup"><span data-stu-id="99873-111">The properties and underlying implementation of personal form library entries include a "Container ID" property that identifies a master container that the local entry must be synchronized with.</span></span> <span data-ttu-id="99873-112">Esto puede ser el identificador de una carpeta arbitrario que contiene los formularios.</span><span class="sxs-lookup"><span data-stu-id="99873-112">This can be the identifier of an arbitrary folder that contains forms.</span></span> <span data-ttu-id="99873-113">Esto es útil si está utilizando el Administrador de un formulario personalizado que es compatible con algún tipo de biblioteca de formularios de toda la organización; el Administrador de formulario se ocupa de la sincronización de los formularios que se almacenan en la biblioteca de formularios personales y la biblioteca de formularios de toda la organización.</span><span class="sxs-lookup"><span data-stu-id="99873-113">This is useful if you are using a custom form manager that supports some sort of organization-wide form library; the form manager would take care of synchronizing the forms stored in the personal form library and the organization-wide form library.</span></span> <span data-ttu-id="99873-114">Esto sucede probablemente cuando el Administrador de formulario se cargó, pero puede suceder en teoría en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="99873-114">This would probably happen when the form manager was loaded, but could theoretically happen at any time.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="99873-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="99873-115">See also</span></span>



[<span data-ttu-id="99873-116">Formularios MAPI</span><span class="sxs-lookup"><span data-stu-id="99873-116">MAPI Forms</span></span>](mapi-forms.md)


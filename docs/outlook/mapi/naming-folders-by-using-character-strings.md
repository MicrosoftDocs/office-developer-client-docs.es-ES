---
title: Asignar nombres a carpetas mediante el uso de las cadenas de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818416"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="11064-103">Asignar nombres a carpetas mediante el uso de las cadenas de caracteres</span><span class="sxs-lookup"><span data-stu-id="11064-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="11064-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11064-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11064-105">Si tiene acceso a una o varias carpetas con frecuencia durante una sesión, considere la posibilidad de asignar nombres a las carpetas con el método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="11064-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="11064-106">Aunque **IMsgStore::SetReceiveFolder** se usa principalmente para establecer carpetas especiales para recibir los mensajes entrantes para las clases de mensaje en particular, también se puede usar para asociar cualquier carpeta con un nombre.</span><span class="sxs-lookup"><span data-stu-id="11064-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="11064-107">El nombre puede ser la misma que la clase de mensaje o puede ser cualquier cadena de caracteres, personalizado para el uso de su cliente.</span><span class="sxs-lookup"><span data-stu-id="11064-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="11064-108">Asociar un nombre a una carpeta, reduce el tiempo necesario para buscar y abrir la carpeta.</span><span class="sxs-lookup"><span data-stu-id="11064-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  


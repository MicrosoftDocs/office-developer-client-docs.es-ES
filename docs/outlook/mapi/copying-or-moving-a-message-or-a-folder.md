---
title: Copiar o mover un mensaje o una carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 97e7c90c2fdc715d7d0749300cc62854fffa6447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563985"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="dbc29-103">Copiar o mover un mensaje o una carpeta</span><span class="sxs-lookup"><span data-stu-id="dbc29-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="dbc29-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbc29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbc29-105">Un cliente puede usar uno de los cuatro métodos para copiar o mover un mensaje o una carpeta:</span><span class="sxs-lookup"><span data-stu-id="dbc29-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="dbc29-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="dbc29-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="dbc29-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="dbc29-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="dbc29-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="dbc29-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="dbc29-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="dbc29-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="dbc29-110">Mediante la configuración de los parámetros y los marcadores adecuados, **CopyTo** y **CopyProps** se pueden establecer para que funcione como **CopyFolder** o **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="dbc29-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="dbc29-111">Tenga en cuenta lo siguiente al decidir qué método de llamada:</span><span class="sxs-lookup"><span data-stu-id="dbc29-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="dbc29-112">¿Copiar o mover una carpeta o un mensaje?</span><span class="sxs-lookup"><span data-stu-id="dbc29-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="dbc29-113">¿Cuánto sabe acerca de la carpeta o el mensaje que se va a mover o copiar?</span><span class="sxs-lookup"><span data-stu-id="dbc29-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="dbc29-114">¿Cuántos de la carpeta o propiedades del mensaje que se va a mover o copiar?</span><span class="sxs-lookup"><span data-stu-id="dbc29-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="dbc29-115">Puede usar los métodos **IMAPIProp** para copiar o mover una carpeta o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="dbc29-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="dbc29-116">**IMAPIFolder::CopyMessages** funciona con los mensajes solamente; **IMAPIFolder::CopyFolder** funciona con carpetas sólo.</span><span class="sxs-lookup"><span data-stu-id="dbc29-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="dbc29-117">Mientras que con los métodos **IMAPIFolder** no requieren ningún conocimiento de las propiedades compatibles con el mensaje para ser copiado o movido o la carpeta, debe tener conocimientos para usar los métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="dbc29-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="dbc29-118">Con **IMAPIProp::CopyProps**, debe especificar cuál de las propiedades de carpeta o mensaje que desee copiar o mover de forma explícita.</span><span class="sxs-lookup"><span data-stu-id="dbc29-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="dbc29-119">Con **IMAPIProp::CopyTo**, a menos que desee copiar o mover todas las propiedades, se debe especificar explícitamente las que se deben excluir.</span><span class="sxs-lookup"><span data-stu-id="dbc29-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="dbc29-120">Para obtener más información acerca de estos métodos, vea [Copiar las propiedades de MAPI](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dbc29-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="dbc29-121">El número de propiedades que se pueden copiar o mover puede afectar a su decisión sobre qué método va a usar.</span><span class="sxs-lookup"><span data-stu-id="dbc29-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="dbc29-122">Si está copiando o moviendo varios mensajes, llame a **IMAPIFolder::CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="dbc29-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="dbc29-123">Una opción alternativa es llamar a **IMAPIProp::CopyProps** para copiar sólo la propiedad de la carpeta **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dbc29-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="dbc29-124">El procedimiento siguiente muestra cómo usar **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="dbc29-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="dbc29-125">Para copiar o mover uno o más mensajes</span><span class="sxs-lookup"><span data-stu-id="dbc29-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="dbc29-126">Busque los identificadores de entrada válido para las carpetas de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="dbc29-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="dbc29-127">Abra estas carpetas en el modo de lectura y escritura mediante una llamada a [IMAPISession::OpenEntry](imapisession-openentry.md) o [IMsgStore::OpenEntry](imsgstore-openentry.md) y establecer el indicador MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="dbc29-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="dbc29-128">Compruebe que el puntero de interfaz devuelto desde **OpenEntry** es un puntero de interfaz **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="dbc29-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="dbc29-129">Si no es así, se convierte en el tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="dbc29-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="dbc29-130">Crear una matriz de identificadores de entrada que representa los mensajes de uno o más para ser copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="dbc29-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="dbc29-131">Llame al método **IMAPIFolder::CopyMessages** con el siguiente conjunto de indicadores:</span><span class="sxs-lookup"><span data-stu-id="dbc29-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="dbc29-132">MESSAGE_MOVE, si desea realizar una operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="dbc29-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="dbc29-133">Controlan MESSAGE_DIALOG y pase una ventana en el parámetro _ulUIParam_ , si desea que la carpeta que se va a mostrar un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="dbc29-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="dbc29-134">Liberar los punteros **IMAPIFolder** para las carpetas de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="dbc29-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="dbc29-135">Si desea copiar el contenido completo de una carpeta a otra carpeta, llame al método de **IMAPIFolder::CopyFolder** o **IMAPIProp::CopyTo** de la carpeta de origen.</span><span class="sxs-lookup"><span data-stu-id="dbc29-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="dbc29-136">Para copiar algunas de las propiedades de una carpeta, llame al método **IMAPIProp::CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="dbc29-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="dbc29-137">Para copiar la mayoría de las propiedades de una carpeta, llamar a **IMAPIProp::CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="dbc29-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="dbc29-138">Por ejemplo, si desea copiar una carpeta **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y las propiedades **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)), tiene las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="dbc29-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="dbc29-139">Llame a **IMAPIFolder::CopyFolder** para copiar todas las propiedades de carpeta y, a continuación, elimine los no deseados de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbc29-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="dbc29-140">Llame a **CopyTo** y todos los de las propiedades de la carpeta excepto **PR_DISPLAY_NAME** y **PR_COMMENT**excluir.</span><span class="sxs-lookup"><span data-stu-id="dbc29-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="dbc29-141">Llamar a **CopyProps**, pasando la matriz de incluir **PR_DISPLAY_NAME** y **PR_COMMENT** .</span><span class="sxs-lookup"><span data-stu-id="dbc29-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="dbc29-142">En este caso, **CopyProps** es la mejor opción porque está diseñada para usarse para copiar un pequeño conjunto de propiedades y es la llamada más fácil implementar.</span><span class="sxs-lookup"><span data-stu-id="dbc29-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="dbc29-143">Para copiar o mover sólo las propiedades de la carpeta, sin incluir los mensajes, llame al método **IMAPIProp::CopyTo** de la carpeta y excluir las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="dbc29-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="dbc29-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dbc29-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="dbc29-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dbc29-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="dbc29-146">Los métodos de copia pueden devolver S_OK, que indica éxito total, MAPI_W_PARTIAL_COMPLETION, que indica éxito parcial o un error.</span><span class="sxs-lookup"><span data-stu-id="dbc29-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="dbc29-147">Si se devuelve MAPI_W_PARTIAL_COMPLETION, utilice la macro **HR_FAILED** para tener acceso a un error más específico.</span><span class="sxs-lookup"><span data-stu-id="dbc29-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="dbc29-148">Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="dbc29-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="dbc29-149">Si copiar mensajes desde el almacén de mensajes de uno a otro y Unicode no es compatible con ambos, tenga en cuenta que la información se puede perder debido a la conversión de página de código.</span><span class="sxs-lookup"><span data-stu-id="dbc29-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="dbc29-150">Normalmente no se puede saber si los almacenes de mensajes admiten formatos de uno o ambos, que no se pueda determinar si se deben copiar las propiedades de texto como cadenas ASCII o como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="dbc29-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="dbc29-151">Si admite Unicode, intenta realizar una copia de Unicode; Si se produce un error con el valor de error MAPI_E_BAD_CHARWIDTH, recurrir a ASCII.</span><span class="sxs-lookup"><span data-stu-id="dbc29-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  


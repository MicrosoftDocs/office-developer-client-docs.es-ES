---
title: OpenStreamOnFile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenStreamOnFile
api_type:
- COM
ms.assetid: 01fa459f-597d-4b16-b340-a79fb270cd71
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b05f5b30eceb7df1bed76c64f4bdda87ede0e463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348632"
---
# <a name="openstreamonfile"></a><span data-ttu-id="2327f-103">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="2327f-103">OpenStreamOnFile</span></span>

  
  
<span data-ttu-id="2327f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2327f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2327f-105">Asigna e inicializa un objeto OLE **IStream** para tener acceso al contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="2327f-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="2327f-106">Esta función toma una cadena ANSI como nombre de archivo que incluye la ruta de acceso y la extensión de archivo, por lo tanto, se recomienda usar la versión Unicode de esta función, [OpenStreamOnFileW](openstreamonfilew.md).</span><span class="sxs-lookup"><span data-stu-id="2327f-106">This function takes an ANSI string as the file name including the path and the file extension, therefore, use of the Unicode version of this function, [OpenStreamOnFileW](openstreamonfilew.md), is recommended.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2327f-107">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="2327f-107">Header file:</span></span>  <br/> |<span data-ttu-id="2327f-108">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="2327f-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2327f-109">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2327f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="2327f-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="2327f-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="2327f-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="2327f-111">Called by:</span></span>  <br/> |<span data-ttu-id="2327f-112">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="2327f-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFile(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPSTR lpszFileName,
  LPSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="2327f-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="2327f-113">Parameters</span></span>

 <span data-ttu-id="2327f-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="2327f-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="2327f-115">a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="2327f-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="2327f-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="2327f-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="2327f-117">a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="2327f-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="2327f-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2327f-118">_ulFlags_</span></span>
  
> <span data-ttu-id="2327f-119">a Máscara de la máscara utilizada para controlar la creación o la apertura del archivo al que se va a tener acceso a través del objeto OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="2327f-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="2327f-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="2327f-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="2327f-121">SOF_UNIQUEFILENAME</span></span> 
  
> <span data-ttu-id="2327f-122">Se debe crear un archivo temporal para el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="2327f-123">Si se establece esta marca, también se deben establecer las marcas STGM_CREATE y STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="2327f-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="2327f-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="2327f-124">STGM_CREATE</span></span> 
  
> <span data-ttu-id="2327f-125">El archivo se creará incluso si ya existe uno.</span><span class="sxs-lookup"><span data-stu-id="2327f-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="2327f-126">Si no se establece el parámetro _lpszFileName_ , se deben establecer tanto este indicador como el STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="2327f-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="2327f-127">Si se establece STGM_CREATE, también se debe establecer la marca STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="2327f-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="2327f-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="2327f-128">STGM_DELETEONRELEASE</span></span> 
  
> <span data-ttu-id="2327f-129">El archivo se eliminará cuando se libere el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="2327f-130">Si no se establece el parámetro _lpszFileName_ , se deben establecer tanto este indicador como el STGM_CREATE.</span><span class="sxs-lookup"><span data-stu-id="2327f-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="2327f-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="2327f-131">STGM_READ</span></span> 
  
> <span data-ttu-id="2327f-132">El archivo se va a crear o abrir con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2327f-132">The file is to be created or opened with read-only access.</span></span> 
    
<span data-ttu-id="2327f-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="2327f-133">STGM_READWRITE</span></span> 
  
> <span data-ttu-id="2327f-134">El archivo se va a crear o abrir con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2327f-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="2327f-135">Si no se establece esta marca, no se debe establecer tampoco la marca STGM_CREATE.</span><span class="sxs-lookup"><span data-stu-id="2327f-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span> 
    
 <span data-ttu-id="2327f-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="2327f-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="2327f-137">a El nombre de archivo, incluida la ruta de acceso y la extensión, del archivo para el que **OpenStreamOnFile** inicializa el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-137">[in] The filename, including path and extension, of the file for which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="2327f-138">Si se establece la marca SOF_UNIQUEFILENAME, _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="2327f-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="2327f-139">Si _lpszFileName_ es null, **OpenStreamOnFile** obtiene una ruta de acceso adecuada del sistema y se deben establecer los dos marcadores STGM_CREATE y STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="2327f-139">If  _lpszFileName_ is NULL, **OpenStreamOnFile** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="2327f-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="2327f-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="2327f-141">a Prefijo del nombre de archivo en el que **OpenStreamOnFile** inicializa el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-141">[in] The prefix for the filename on which **OpenStreamOnFile** initializes the **IStream** object.</span></span> <span data-ttu-id="2327f-142">Si se establece, el prefijo no debe contener más de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="2327f-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="2327f-143">Si _lpszPrefix_ es null, se usa un prefijo de "Sof".</span><span class="sxs-lookup"><span data-stu-id="2327f-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="2327f-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="2327f-144">_lppStream_</span></span>
  
> <span data-ttu-id="2327f-145">contempla Puntero a un puntero a un objeto que expone la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2327f-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2327f-146">Return value</span></span>

<span data-ttu-id="2327f-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="2327f-147">S_OK</span></span> 
  
> <span data-ttu-id="2327f-148">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="2327f-148">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="2327f-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2327f-149">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2327f-150">No se pudo tener acceso al archivo debido a que los permisos de usuario son insuficientes o a que no se pueden modificar los archivos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2327f-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span> 
    
<span data-ttu-id="2327f-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2327f-151">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2327f-152">El archivo designado no existe.</span><span class="sxs-lookup"><span data-stu-id="2327f-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2327f-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2327f-153">Remarks</span></span>

<span data-ttu-id="2327f-154">La función **OpenStreamOnFile** tiene dos usos importantes, que se distinguen por la configuración de la marca SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="2327f-154">The **OpenStreamOnFile** function has two important uses, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="2327f-155">Si no se establece este indicador, **OpenStreamOnFile** abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de un dato adjunto mediante **IStream. :: CopyTo** (método).</span><span class="sxs-lookup"><span data-stu-id="2327f-155">When this flag is not set, **OpenStreamOnFile** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="2327f-156">En este caso, el parámetro _lpszFileName_ especifica la ruta de acceso y el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="2327f-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="2327f-157">Cuando se establece SOF_UNIQUEFILENAME, **OpenStreamOnFile** crea un archivo temporal para contener los datos de un objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="2327f-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFile** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="2327f-158">Para este uso, el parámetro _lpszFileName_ puede designar opcionalmente la ruta de acceso al directorio en el que se va a crear el archivo, y el parámetro _lpszPrefix_ puede especificar opcionalmente un prefijo para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="2327f-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="2327f-159">Cuando finaliza la aplicación cliente o el proveedor de servicios que realiza la llamada con el objeto **IStream** , debe liberarla llamando al método OLE **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="2327f-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="2327f-160">MAPI usa las funciones a las que apunta _lpAllocateBuffer_ y _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a interfaces de objeto como [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="2327f-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2327f-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="2327f-161">Notes to callers</span></span>

<span data-ttu-id="2327f-162">La marca SOF_UNIQUEFILENAME se usa para crear un archivo temporal con un nombre único para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="2327f-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="2327f-163">Si se establece esta marca, el parámetro _lpszFileName_ especifica la ruta de acceso del archivo temporal y el parámetro _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="2327f-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="2327f-164">El nombre de archivo <prefix>construido es HHHH TMP, donde HHHH es un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2327f-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="2327f-165">Si _lpszFileName_ es null, el archivo se creará en el directorio de archivos temporales que devuelve la función de Windows **GetTempPath**, o el directorio actual, si no se ha designado ningún directorio de archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="2327f-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span> 
  
<span data-ttu-id="2327f-166">Si no se establece la marca SOF_UNIQUEFILENAME, se omite _lpszPrefix_ y _lpszFileName_ debe contener la ruta de acceso completa y el nombre de archivo del archivo que se va a abrir o crear.</span><span class="sxs-lookup"><span data-stu-id="2327f-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="2327f-167">El archivo se abrirá o se creará en función de los demás indicadores establecidos en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="2327f-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2327f-168">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2327f-168">MFCMAPI reference</span></span>

<span data-ttu-id="2327f-169">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2327f-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2327f-170">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2327f-170">**File**</span></span>|<span data-ttu-id="2327f-171">**Función**</span><span class="sxs-lookup"><span data-stu-id="2327f-171">**Function**</span></span>|<span data-ttu-id="2327f-172">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2327f-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2327f-173">Archivo. cpp</span><span class="sxs-lookup"><span data-stu-id="2327f-173">File.cpp</span></span>  <br/> |<span data-ttu-id="2327f-174">WriteAttachStreamToFile</span><span class="sxs-lookup"><span data-stu-id="2327f-174">WriteAttachStreamToFile</span></span>  <br/> |<span data-ttu-id="2327f-175">MFCMAPI usa el método **OpenStreamOnFile** para abrir un objeto Stream en un archivo para que se puedan escribir datos adjuntos en él.</span><span class="sxs-lookup"><span data-stu-id="2327f-175">MFCMAPI uses the **OpenStreamOnFile** method to open a stream on a file so an attachment can be written out to it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2327f-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="2327f-176">See also</span></span>



[<span data-ttu-id="2327f-177">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2327f-177">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


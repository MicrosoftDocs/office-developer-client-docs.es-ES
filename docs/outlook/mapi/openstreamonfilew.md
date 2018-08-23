---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dc8644a658b8aca97f80fcf0a942551509064bd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581562"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="c9113-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="c9113-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="c9113-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9113-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9113-105">Asigna e inicializa un objeto **IStream** OLE para tener acceso al contenido de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c9113-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="c9113-106">Esta función toma las cadenas UNICODE como argumentos, a diferencia de la versión ANSI de esta función [OpenStreamOnFile](openstreamonfile.md)y por lo tanto caracteres arbitrarios en el nombre de archivo incluye la ruta de acceso y la extensión.</span><span class="sxs-lookup"><span data-stu-id="c9113-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9113-107">Exportada por:</span><span class="sxs-lookup"><span data-stu-id="c9113-107">Exported by:</span></span>  <br/> |<span data-ttu-id="c9113-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c9113-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c9113-109">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="c9113-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9113-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="c9113-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="c9113-111">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="c9113-111">Called by:</span></span>  <br/> |<span data-ttu-id="c9113-112">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="c9113-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="c9113-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9113-113">Parameters</span></span>

 <span data-ttu-id="c9113-114">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="c9113-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c9113-115">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="c9113-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c9113-116">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="c9113-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c9113-117">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="c9113-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c9113-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9113-118">_ulFlags_</span></span>
  
> <span data-ttu-id="c9113-119">[entrada] Máscara de bits de indicadores que se utilizan para controlar la creación o apertura del archivo para tener acceso a través del objeto **IStream** OLE.</span><span class="sxs-lookup"><span data-stu-id="c9113-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="c9113-120">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="c9113-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="c9113-121">SOF_UNIQUEFILENAME</span><span class="sxs-lookup"><span data-stu-id="c9113-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="c9113-122">Es un archivo temporal que se creará para el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9113-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="c9113-123">Si se establece este marcador, también se deben establecer los indicadores STGM_CREATE y STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="c9113-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="c9113-124">STGM_CREATE</span><span class="sxs-lookup"><span data-stu-id="c9113-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="c9113-125">Es el archivo que se creará, incluso si ya existe una.</span><span class="sxs-lookup"><span data-stu-id="c9113-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="c9113-126">Si no se establece el parámetro _lpszFileName_ , se deben establecer este indicador y el STGM_DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="c9113-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="c9113-127">Si se establece STGM_CREATE, también se debe establecer la marca STGM_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="c9113-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="c9113-128">STGM_DELETEONRELEASE</span><span class="sxs-lookup"><span data-stu-id="c9113-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="c9113-129">Es el archivo que se eliminará cuando se libera el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9113-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="c9113-130">Si no se establece el parámetro _lpszFileName_ , se deben establecer este indicador y el STGM_CREATE.</span><span class="sxs-lookup"><span data-stu-id="c9113-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="c9113-131">STGM_READ</span><span class="sxs-lookup"><span data-stu-id="c9113-131">STGM_READ</span></span>
  
> <span data-ttu-id="c9113-132">El archivo es que se creen o se abrió con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9113-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="c9113-133">STGM_READWRITE</span><span class="sxs-lookup"><span data-stu-id="c9113-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="c9113-134">Es el archivo que se creó o se abran con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c9113-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="c9113-135">Si no se establece este indicador, el indicador STGM_CREATE no debe establecerse cualquiera.</span><span class="sxs-lookup"><span data-stu-id="c9113-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="c9113-136">_lpszFileName_</span><span class="sxs-lookup"><span data-stu-id="c9113-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="c9113-137">[entrada] El nombre de archivo, incluida la ruta de acceso y la extensión del Unicode con nombre de archivo para el que **OpenStreamOnFileW** inicializa el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9113-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="c9113-138">Si se establece la marca SOF_UNIQUEFILENAME, _lpszFileName_ contiene la ruta de acceso al directorio en el que se va a crear un archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="c9113-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="c9113-139">Si _lpszFileName_ es NULL, **OpenStreamOnFileW** Obtiene una ruta de acceso apropiado desde el sistema y se deben establecer el STGM_CREATE y la STGM_DELETEONRELEASE marcas.</span><span class="sxs-lookup"><span data-stu-id="c9113-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="c9113-140">_lpszPrefix_</span><span class="sxs-lookup"><span data-stu-id="c9113-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="c9113-141">[entrada] El prefijo del nombre de archivo de Unicode en la que **OpenStreamOnFileW** inicializa el objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9113-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="c9113-142">Si se establece, el prefijo debe contener no más de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="c9113-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="c9113-143">Si _lpszPrefix_ es NULL, se utiliza un prefijo de "SOF".</span><span class="sxs-lookup"><span data-stu-id="c9113-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="c9113-144">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="c9113-144">_lppStream_</span></span>
  
> <span data-ttu-id="c9113-145">[out] Puntero a un puntero a un objeto que expone la interfaz **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9113-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9113-146">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9113-146">Return value</span></span>

<span data-ttu-id="c9113-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9113-147">S_OK</span></span>
  
> <span data-ttu-id="c9113-148">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="c9113-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c9113-149">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c9113-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="c9113-150">No se pudo tener acceso el archivo debido a los permisos de usuario suficientes o debido a que no se pueden modificar los archivos de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="c9113-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="c9113-151">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c9113-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="c9113-152">No existe el archivo designado.</span><span class="sxs-lookup"><span data-stu-id="c9113-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9113-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9113-153">Remarks</span></span>

<span data-ttu-id="c9113-154">La función **OpenStreamOnFileW** tiene dos usos importantes además de tratar un archivo con un nombre de Unicode, diferenciado por la configuración de la marca SOF_UNIQUEFILENAME.</span><span class="sxs-lookup"><span data-stu-id="c9113-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="c9113-155">Cuando no se establece este marcador, **OpenStreamOnFileW** se abre un objeto **IStream** en un archivo existente, por ejemplo, para copiar su contenido en la propiedad **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de los datos adjuntos con el ** IStream:: CopyTo** (método).</span><span class="sxs-lookup"><span data-stu-id="c9113-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="c9113-156">En este caso, el parámetro _lpszFileName_ especifica la ruta de acceso y el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="c9113-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="c9113-157">Cuando se establece SOF_UNIQUEFILENAME, **OpenStreamOnFileW** crea un archivo temporal para contener datos para un objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9113-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="c9113-158">Para este uso, el parámetro _lpszFileName_ , opcionalmente, puede designar la ruta de acceso al directorio donde es el archivo que se creará y el parámetro _lpszPrefix_ , opcionalmente, puede especificar un prefijo para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c9113-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="c9113-159">Cuando finalice la aplicación cliente que llama o el proveedor de servicios con el objeto **IStream** , que debe liberar llamando al método OLE **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="c9113-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="c9113-160">MAPI utiliza las funciones que señala _lpAllocateBuffer_ y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto como [IMAPIProp:: GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="c9113-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9113-161">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="c9113-161">Notes to callers</span></span>

<span data-ttu-id="c9113-162">El indicador SOF_UNIQUEFILENAME se utiliza para crear un archivo temporal con un nombre único para el sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="c9113-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="c9113-163">Si se establece este indicador, el _lpszFileName_ parámetro especifica la ruta de acceso para el archivo temporal y el parámetro _lpszPrefix_ contiene los caracteres de prefijo del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c9113-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="c9113-164">Es el nombre de archivo construido <prefix>HHHH. TMP, donde HHHH es un número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="c9113-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="c9113-165">Si _lpszFileName_ es NULL, el archivo se creará en el directorio de archivos temporales que se devuelve desde la función de Windows **GetTempPath**o el directorio actual si no se ha designado ningún directorio de archivos temporales.</span><span class="sxs-lookup"><span data-stu-id="c9113-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="c9113-166">Si no está establecido el indicador SOF_UNIQUEFILENAME, se omite _lpszPrefix_ y _lpszFileName_ debe contener la ruta de acceso completa y el nombre del archivo que se va a abrir o crear.</span><span class="sxs-lookup"><span data-stu-id="c9113-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="c9113-167">El archivo se va a abrir o crear en función de los otros marcadores que se establecen en _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c9113-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9113-168">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c9113-168">See also</span></span>



[<span data-ttu-id="c9113-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="c9113-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

